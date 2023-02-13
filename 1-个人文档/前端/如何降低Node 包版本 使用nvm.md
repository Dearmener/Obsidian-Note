> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.cnblogs.com](https://www.cnblogs.com/luoguixin/p/16275502.html)

> 降低 node 版本的方法：首先全局安装 n 模块；然后通过 “n rm v8.16.0” 卸载指定的 node 版本；接着安装 nvm；最后通过 “nvm use 10.16.2” 安装指定版本即可。

![](https://img.php.cn/upload/article/202103/03/2021030311113264723.jpg)

本文操作环境：windows7 系统、nodejs10.16.2 版，DELL G3 电脑。
  
**Node 版本的升级和降级**

在开发的工程中，我们可能需要经常切换 node 版本来应对不同的开发环境，所以需要经常使用不同版本的 node

## 一、安装 npm 插件 n , 通过 n 模块来管理 node 版本

1、全局安装 n 模块

```
npm install -g n<br>或<br>npm i -g n --force
```

2、安装当前稳定版本

```
n stable或者sudo n stable
```

3、安装最新版本的

```
n latest或者sudo n latest
```

4、安装指定版本的 node

```
n v8.16.0
```

5、卸载指定的 node 版本

```
n rm v8.16.0
```

【推荐：[nodejs 视频教程](https://www.php.cn/course/list/24.html)】

## 二、使用 nvm 管理 node 版本

1、安装 nvm

```
brew install nvm
```

2、使用 nvm 安装 node 版本

安装最新版本

```
nvm isntall node
```

安装指定版本

```
nvm install 8.16.0
```

3、查看所有版本

```
nvm ls
```

4、切换 node 版本

使用最新版本

```
nvm use node
```

使用指定版本

```
nvm use 10.16.2
```

通常我会使用第二种方式

例如：我在一个项目中使用的是 node@6.13.2, 新项目使用的是 node@8.16.0,

先要安装 node@8.16.0，nvm install 8.16.0，

然后，nvm use 8.16.0