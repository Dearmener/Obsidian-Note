### 标识符和关键字的区别是什么？
在我们编写程序的时候，需要大量地为程序、类、变量、方法等取名字，于是就有了 **标识符** 。简单来说， **标识符就是一个名字** 。
有一些标识符，Java 语言已经赋予了其特殊的含义，只能用于特定的地方，这些特殊的标识符就是 **关键字** 。简单来说，**关键字是被赋予特殊含义的标识符** 。比如，在我们的日常生活中，如果我们想要开一家店，则要给这个店起一个名字，起的这个“名字”就叫标识符。但是我们店的名字不能叫“警察局”，因为“警察局”这个名字已经被赋予了特殊的含义，而“警察局”就是我们日常生活中的关键字。

### 对象的相等和引用相等的区别
- 对象的相等一般比较的是内存中存放的内容是否相等。
    - 注意：如果你的类里面没有重写equals方法，那么从Object类中继承的equals方法比较的仍然是对象指向的内存地址，得到的结果仍然是false。所以，如果要比较对象的值是否相等，要在类中重写equals方法进行比较。
- 引用相等一般比较的是他们指向的内存地址是否相等。
- 在Object类中有一个equals方法用于比较 2 个对象的内存地址是否相等，String 类对该方法进行了重写以用于比较字符串的值是否相等。
> [!NOTE] 补充：如何重写equals方法
> 重写 equals 方法的步骤如下：
> 1. 在你的类中添加一个方法，使用 public boolean equals(Object o) 作为方法签名。
> 2. 在方法体内, 判断如果传入的对象和当前对象是同一个对象，那么直接返回 true
> 3. 判断传入的对象是否为 null, 或者是否是同类型的对象, 如果不是返回 false.
> 4. 将传入的对象转换为你的类类型的对象
> 5. 比较你的类的所有关键属性是否相等.
> 6. 返回比较结果.
下面是一个简单的示例:
```java
class Person {
    private String name;
    private int age;
    // constructor, getters and setters
    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Person person = (Person) o;
        return age == person.age &&
               Objects.equals(name, person.name);
    }
}
```

### 继承
不同类型的对象，相互之间经常有一定数量的共同点。例如，小明同学、小红同学、小李同学，都共享学生的特性（班级、学号等）。同时，每一个对象还定义了额外的特性使得他们与众不同。例如小明的数学比较好，小红的性格惹人喜爱；小李的力气比较大。继承是使用已存在的类的定义作为基础建立新类的技术，新类的定义可以增加新的数据或新的功能，也可以用父类的功能，但不能选择性地继承父类。通过使用继承，可以快速地创建新的类，可以提高代码的重用，程序的可维护性，节省大量创建新类的时间 ，提高我们的开发效率。
**关于继承如下 3 点请记住：**
1.  子类拥有父类对象所有的属性和方法（包括私有属性和私有方法），但是父类中的私有属性和方法子类是无法访问，**只是拥有**。
2.  子类可以拥有自己属性和方法，即子类可以对父类进行扩展。
3.  子类可以用自己的方式实现父类的方法。（以后介绍）。

### 接口和抽象类有什么共同点和区别？
**共同点** ：
- 都不能被实例化。 
- 都可以包含抽象方法。
- 都可以有默认实现的方法（Java 8 可以用 `default` 关键字在接口中定义默认方法）。
**区别** ：
- 接口主要用于对类的行为进行约束，你实现了某个接口就具有了对应的行为。抽象类主要用于代码复用，强调的是所属关系。
- 一个类只能继承一个类，但是可以实现多个接口。
- 接口中的成员变量只能是 `public static final` 类型的，不能被修改且必须有初始值，而抽象类的成员变量默认 default，可在子类中被重新定义，也可被重新赋值。

### 深拷贝和浅拷贝区别了解吗-什么是引用拷贝
![[Pasted image 20230116213258.png]]
假如有个Person类，浅拷贝，会在堆中创建一个新的Person对象。如果Person对象中有一个引用类型的参数（Address），则浅拷贝会共用同一个Address对象，深拷贝会新建一个Address对象。
关于深拷贝和浅拷贝区别，我这里先给结论：
- **浅拷贝**：浅拷贝会在堆上创建一个新的对象区别于引用拷贝的一点），不过，如果原对象内部的属性是引用类型的话，浅拷贝会直接复制内部对象的引用地址，也就是说拷贝对象和原对象共用同一个内部对象。
- **深拷贝** ：深拷贝会完全复制整个对象，包括这个对象所包含的内部对象，即两个对象毫无关系。
- **引用拷贝**：引用拷贝在堆中只有一个对象，不同的变量名指向堆中相同的对象。
> 实现浅拷贝（使用clone）
```java 
public class Address implements Cloneable{  
    private String name;  
    // 省略构造函数、Getter&Setter方法  
    @Override  
    public Address clone() {  
        try {  
            return (Address) super.clone();  
        } catch (CloneNotSupportedException e) {  
            throw new AssertionError();  
        }  
    }}  
public class Person implements Cloneable {  
    private Address address;  
    // 省略构造函数、Getter&Setter方法  
    @Override  
    public Person clone() {  
        try {  
            Person person = (Person) super.clone();  
            return person;  
        } catch (CloneNotSupportedException e) {  
            throw new AssertionError();  
        }  
    }}
```
> 实现深拷贝（使用clone）
```java
@Override  
public Person clone() {  
    try {  
        Person person = (Person) super.clone();  
        person.setAddress(person.getAddress().clone());  
        return person;  
    } catch (CloneNotSupportedException e) {  
        throw new AssertionError();  
    }  
}
```
> [!Warining] 使用clone实现浅拷贝和深拷贝时，要在类上实现Cloneable接口

### String 为什么是不可变的?
`String` 类中使用 `final` 关键字修饰字符数组来保存字符串，~~所以`String` 对象是不可变的。~~
```Java
public final class String implements java.io.Serializable, Comparable<String>, CharSequence {
    private final char value[];
	//...
}
```

> 🐛 修正 ： 我们知道被 `final` 关键字修饰的类不能被继承，修饰的方法不能被重写，修饰的变量是基本数据类型则值不能改变，修饰的变量是引用类型则不能再指向其他对象。因此，`final` 关键字修饰的数组保存字符串并不是 `String` 不可变的根本原因，因为这个数组保存的字符串是可变的（`final` 修饰引用类型变量的情况）。
> 
> `String` 真正不可变有下面几点原因：
> 
> 1.  保存字符串的数组被 `final` 修饰且为私有的，并且`String` 类没有提供/暴露修改这个字符串的方法。
> 2.  `String` 类被 `final` 修饰导致其不能被继承，进而避免了子类破坏 `String` 不可变。



