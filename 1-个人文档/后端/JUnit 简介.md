> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [juejin.cn](https://juejin.cn/post/7158258490501234695)

> 之前把我的 [mall 项目升级到 Spring Boot 2.7](https://juejin.cn/post/7116694234236715038 "https://juejin.cn/post/7116694234236715038") 的时候，很多之前的测试方法都不能用了，原来是 Spring Boot Test 已经升级支持 JUnit 5 了。今天我们来聊聊新版 Spring Boot Test 的使用，有了它，我们就不需要再使用 main 方法来测试了！

SpringBoot 实战电商项目 mall（50k+star）地址：[github.com/macrozheng/…](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2Fmacrozheng%2Fmall "https://github.com/macrozheng/mall")

## JUnit 简介
--------
JUnit 是一款 Java 语言的单元测试框架，目前大多数 Java 开发环境都已经支持它了。JUnit 测试也就是所谓的白盒测试，在程序员知道程序内部逻辑的基础上进行的测试，使用 JUnit 能让我们快速地完成单元测试。Spring Boot Test 将 JUnit 和其他测试框架结合起来，提供了便捷高效的测试手段，目前 Spring Boot 2.7 版本采用的是 JUnit 5。

### 常用注解
> 在使用 Spring Boot Test 之前，我们先来了解下它常用的注解，这对使用它很有帮助，具体参考下表即可！

<table><thead><tr><th>注解</th><th>作用</th></tr></thead><tbody><tr><td>@SpringBootTest</td><td>用于指定测试类启用 Spring Boot Test，默认会提供 Mock 环境</td></tr><tr><td>@ExtendWith</td><td>如果只想启用 Spring 环境进行简单测试，不想启用 Spring Boot 环境，可以配置扩展为：SpringExtension</td></tr><tr><td>@Test</td><td>指定方法为测试方法</td></tr><tr><td>@TestMethodOrder</td><td>用于配置测试类中方法的执行顺序策略，配置为 OrderAnnotation 时，按 @Order 顺序执行</td></tr><tr><td>@Order</td><td>用于配置方法的执行顺序，数字越低执行顺序越高</td></tr><tr><td>@DisplayName</td><td>用于指定测试类和测试方法的别名</td></tr><tr><td>@BeforeAll</td><td>在测试类的所有测试方法前执行一次，可用于全局初始化</td></tr><tr><td>@AfterAll</td><td>在测试类的所有测试方法后执行一次，可用于全局销毁资源</td></tr><tr><td>@BeforeEach</td><td>在测试类的每个测试方法前都执行一次</td></tr><tr><td>@AfterEach</td><td>在测试类的每个测试方法后都执行一次</td></tr><tr><td>@Disabled</td><td>禁用测试方法</td></tr><tr><td>@RepeatedTest</td><td>指定测试方法重复执行</td></tr><tr><td>@ParameterizedTest</td><td>指定参数化测试方法，类似重复执行，从 @ValueSource 中获取参数</td></tr><tr><td>@ValueSource</td><td>用于参数化测试指定参数</td></tr><tr><td>@AutoConfigureMockMvc</td><td>启用 MockMvc 的自动配置，可用于测试接口</td></tr></tbody></table>

## 基本使用
----
> 下面我们来聊聊这些注解的基本使用，通过它们可以实现一些基本的单元测试。

### 集成 Spring Boot Test
如果你想在项目中集成 Spring Boot Test 的话，需要先在`pom.xml`中添加如下依赖。
``` xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
    <scope>test</scope>
</dependency>
复制代码
```
### 最简单的测试
*   我们先来一个最简单的单元测试，使用`@SpringBootTest`注解启用单元测试，使用`@Test`指定测试方法，使用`Assertions`类的方法来断言结果是否符合预期，具体代码如下。
``` java
/**
 * JUnit基本测试
 * Created by macro on 2022/10/11.
 */
@SpringBootTest
public class FirstTest {
    @Test
    public void test() {
        int a=1;
        Assertions.assertEquals(1,a);
    }
}
复制代码
```
*   然后点击测试方法左侧按钮即可进行测试。
![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9c5b84c34b644b738ca42b52517a0180~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

*   执行完成后我们在 IDEA 的执行窗口中就可以看到方法测试通过了，由于使用`@SpringBootTest`启用了 Spring Boot 环境，日志中会输出 Spring Boot 的 banner。
![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/92d6b8c3a3e34dbba5bd6081d9efc6a7~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

### 指定测试方法顺序

*   我们可以通过`@TestMethodOrder`注解和`@Order`注解来指定所有测试方法的执行顺序，具体代码如下。
``` java
/**
 * JUnit指定方法测试顺序
 * Created by macro on 2022/10/10.
 */
@ExtendWith(SpringExtension.class)
@TestMethodOrder(MethodOrderer.OrderAnnotation.class)
public class MethodOrderTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(MethodOrderTest.class);

    @Test
    @Order(1)
    @DisplayName("order为1的方法")
    void lowOrder(){
        LOGGER.info("lowOrder method");
    }

    @Test
    @Order(10)
    @DisplayName("order为10的方法")
    void highOrder(){
        LOGGER.info("highOrder method");
    }
}
复制代码
```

*   点击类左侧测试按钮，可以直接运行该类中的所有测试方法。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0beed68a33a44a07b07de1ac25633a54~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

*   这里由于我们使用了`@DisplayName`注解给测试方法取了个别名，而且我们使用了`@ExtendWith`指定了运行环境为 Spring 而不是 Spring Boot，所以日志中不会出现 Spring Boot 的 banner，执行速度也更快。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/420afcbde9274319a2dc6868327f08ec~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

### 生命周期测试

*   我们还可以通过 JUnit 5 的生命周期注解来执行测试方法，比如在`@BeforeAll`注解指定的方法中做全局初始化，在`@AfterAll`注解指定的方法中做资源的销毁，具体代码如下。

``` java
/**
 * JUnit生命周期测试
 * Created by macro on 2022/10/10.
 */
@ExtendWith(SpringExtension.class)
public class LifecycleTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(LifecycleTest.class);

    @BeforeAll
    static void allInit(){
        LOGGER.info("allInit()：在所有方法前执行，只执行一次");
    }

    @BeforeEach
    void eachInit(){
        LOGGER.info("eachInit()：在测试方法前执行，每个测试方法前都执行");
    }

    @Test
    void successTest() {
        LOGGER.info("successTest()：方法执行成功");
    }

    @AfterEach
    void eachDown(){
        LOGGER.info("eachDown()：在测试方法后执行，每个测试方法后都执行");
    }

    @AfterAll
    static void allDown(){
        LOGGER.info("allDown()：在测试方法后执行，每个测试方法后都执行");
    }

}
复制代码
```

*   测试完成后，控制台输出日志如下。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6b7342e553134d87adfac893593390a5~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

### 断言的使用

> 我们可以通过`Assertions`类中提供的断言 API 来断言测试结果。

*   例如我们可以使用`fail`方法直接断言方法执行失败并输出提示信息。

``` java
/**
 * JUnit断言测试
 * Created by macro on 2022/10/11.
 */
@ExtendWith(SpringExtension.class)
public class AssertTest {

    @Test
    void failTest() {
        Assertions.fail("failTest()：方法执行失败");
    }
}
复制代码
```

*   测试方法执行后会直接抛出异常信息。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a119f9dd6bd448249c4e11bf9d9c89fe~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

*   还可以通过`assertTrue`、`assertNull`、`assertEquals`这类方法来断言结果是否符合预期。

``` java
/**
 * JUnit断言测试
 * Created by macro on 2022/10/11.
 */
@ExtendWith(SpringExtension.class)
public class AssertTest {

    @Test
    void failTest() {
        Assertions.fail("failTest()：方法执行失败");
    }

    @Test
    void trueTest(){
        Assertions.assertTrue(1==1);
    }

    @Test
    void trueFalse(){
        Assertions.assertFalse(3<=2);
    }

    @Test
    void nullTest(){
        String str = null;
        Assertions.assertNull(str);
    }

    @Test
    void notNullTest(){
        String str = "test";
        Assertions.assertNotNull(str);
    }

    @Test
    void equalsTest(){
        String str1 = "test";
        String str2 = "test";
        Assertions.assertEquals(str1,str2);
    }

    @Test
    void notEqualsTest(){
        String str1 = "test";
        String str2 = "test";
        Assertions.assertNotEquals(str1,str2);
    }
}
复制代码
```

*   也可以使用`assertThrows`方法来断言方法中抛出的异常。

``` java
/**
 * JUnit断言测试
 * Created by macro on 2022/10/11.
 */
@ExtendWith(SpringExtension.class)
public class AssertTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(LifecycleTest.class);
    @Test
    void throwsTest(){
        Assertions.assertThrows(NullPointerException.class,()->{
            String str = null;
            LOGGER.info(str.toLowerCase());
        });
    }
}
复制代码
```

*   还可通过`assertTimeout`方法断言方法的执行时间。

``` java
/**
 * JUnit断言测试
 * Created by macro on 2022/10/11.
 */
@ExtendWith(SpringExtension.class)
public class AssertTest {
    @Test
    void timeoutTest(){
        Assertions.assertTimeout(Duration.ofMillis(1000),()->{
            long sleepTime = 2000;
            ThreadUtil.sleep(sleepTime);
            LOGGER.info("timeoutTest():休眠{}毫秒",sleepTime);
        });
    }
}
复制代码
```

*   或者通过`assertAll`方法将几个断言结合起来使用，`Assertions`类中提供的工具方法很多，具体可以参考它的代码。

``` java
/**
 * JUnit断言测试
 * Created by macro on 2022/10/11.
 */
@ExtendWith(SpringExtension.class)
public class AssertTest {
    @Test
    void assertAllTest(){
        Assertions.assertAll(()->{
            trueTest();
        },()->{
            nullTest();
        },()->{
            equalsTest();
        });
    }
}
复制代码
```

### 其他测试
*   Spring Boot Test 除了上述测试功能，还可以使用`@Disabled`来禁用某个测试方法。
``` java
/**
 * JUnit其他测试
 * Created by macro on 2022/10/10.
 */
@ExtendWith(SpringExtension.class)
public class OtherTest {
    @Test
    @Disabled("用于测试@Disabled注解")
    void disabledTest() {
        LOGGER.info("disabledTest()：方法被执行");
    }
}
复制代码
```

*   也可以使用`@RepeatedTest`来实现循环测试。
``` java
/**
 * JUnit其他测试
 * Created by macro on 2022/10/10.
 */
@ExtendWith(SpringExtension.class)
public class OtherTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(LifecycleTest.class);
    private static int count = 0;

    @RepeatedTest(3)
    void repeatedTest() {
        count++;
        LOGGER.info("repeatedTest()：重复执行第{}次",count);
    }
}
复制代码
```

*   还可以通过`@ParameterizedTest`来进行参数化测试。
``` java
/**
 * JUnit其他测试
 * Created by macro on 2022/10/10.
 */
@ExtendWith(SpringExtension.class)
public class OtherTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(LifecycleTest.class);

    @ParameterizedTest
    @ValueSource(ints = {1,2,3})
    public void parameterizedTest(int a){
        LOGGER.info("parameterizedTest()：a={}",a);
    }
}
复制代码
```

*   运行以上测试方法后，具体测试结果如下。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/17a5bba1d82845beb55e2bb5a1c917d3~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

项目实战
----

> 上面介绍了 Spring Boot Test 的基本使用，下面我们结合项目来使用下它。

### Dao 层测试

如果我们的项目需要对数据访问层 Dao 中的方法进行测试的话，直接注入 Mapper 接口，在测试方法中直接调用即可，这里对根据 ID 查询品牌的 Mapper 方法进行测试。

``` java
/**
 * Dao层方法测试
 * Created by macro on 2022/10/11.
 */
@SpringBootTest
public class MapperTest {

    private static final Logger LOGGER = LoggerFactory.getLogger(MapperTest.class);

    @Autowired
    private PmsBrandMapper brandMapper;

    @Test
    void testGetById(){
        long id = 6;
        PmsBrand pmsBrand = brandMapper.selectByPrimaryKey(id);
        LOGGER.info("brand name:{}",pmsBrand.getName());
        Assertions.assertEquals("小米",pmsBrand.getName());
    }
}
复制代码
```

Service 层测试
-----------

对业务层 Service 中的方法测试也是一样的，直接注入 Service 接口，在测试方法中直接调用即可，这里对根据 ID 查询品牌的 Service 方法进行测试。

``` java
/**
 * Service层方法测试
 * Created by macro on 2022/10/11.
 */
@SpringBootTest
public class ServiceTest {
    private static final Logger LOGGER = LoggerFactory.getLogger(ServiceTest.class);
    @Autowired
    private PmsBrandService brandService;

    @Test
    void testGetById(){
        long id = 6;
        PmsBrand pmsBrand = brandService.getBrand(id);
        LOGGER.info("brand name:{}",pmsBrand.getName());
        Assertions.assertEquals("小米",pmsBrand.getName());
    }
}
复制代码
```

Controller 层测试
--------------

对于 Controller 层方法进行测试，有时我们需要模拟请求，使用 MockMvc 即可，这里模拟测试下分页查询品牌列表的接口。

``` java
/**
 * Controller层方法测试
 * Created by macro on 2022/10/11.
 */
@SpringBootTest
@AutoConfigureMockMvc
public class ControllerTest {

    @Autowired
    private MockMvc mockMvc;

    @Test
    void mvcTest() throws Exception{
        //模拟发送一个请求访问分页查询品牌列表的接口
        mockMvc.perform(MockMvcRequestBuilders.get("/brand/list") //设置请求地址
                .param("pageNum","1") //设置请求参数
                .param("pageSize","5"))
                .andExpect(MockMvcResultMatchers.status().isOk()) //断言返回状态码为200
                .andDo(MockMvcResultHandlers.print()) //在控制台打印日志
                .andReturn(); //返回请求结果
    }
}
复制代码
```

由于我们选择了在控制台输出日志，控制台将输出如下信息。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1e43a56778d54df780a74589fca90483~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

总结
--

今天带大家体验了一把 Spring Boot Test，作为 Spring Boot 官方测试框架，确实功能很强大。由于其主要基于 JUnit 5，和 JUnit 5 的用法基本一致。使用它进行单元测试，无需启动整个项目，更快更好用！

参考资料
----

JUnit 5 官方文档：[junit.org/junit5/docs…](https://link.juejin.cn?target=https%3A%2F%2Fjunit.org%2Fjunit5%2Fdocs%2Fcurrent%2Fuser-guide%2F "https://junit.org/junit5/docs/current/user-guide/")

项目源码地址
------

[github.com/macrozheng/…](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2Fmacrozheng%2Fmall-learning%2Ftree%2Fmaster%2Fmall-tiny-test "https://github.com/macrozheng/mall-learning/tree/master/mall-tiny-test")