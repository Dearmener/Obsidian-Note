### 一、Tauri初识

官方文档：[传送门](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2F "https://tauri.app/")

> `Tauri`是一个为多平台部署构建优化、安全且独立于前端的应用程序，可使用 Web 技术为所有主要桌面操作系统构建软件。
> 
> 主要特点是 构建更小、更快、更安全的桌面应用程序。
> 
> 核心库是用`Rust`编写的，用户界面几乎可以使用任何前端框架编写。
> 
> 它采用Rust作为后端服务，前端采用`TAO`、`WRY`等库来提供轻量级的webview，最终将呈现的是更小的包和更小的内存消耗。

#### 1\. Rust

[![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/427af62500a741829bd1ee0ece2b064e~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)
](https://link.juejin.cn/?target=https%3A%2F%2Fdoc.rust-lang.org "https://doc.rust-lang.org")

> Rust 语言最早发布于 2014 年 9 月。
> 是一种高效、可靠的通用高级语言，其高效不仅限于开发效率，它的执行效率也是令人称赞的，是一种少有的兼顾开发效率和执行效率的语言，且内存利用率极高。

#### 2\. TAO
[![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9a31005adc2b47d898eddf3bc4898f5f~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)
](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Ftauri-apps%2Ftao "https://github.com/tauri-apps/tao")

> Rust中的跨平台`应用程序窗口创建库`，支持所有主要平台，如Windows、macOS、Linux、iOS和Android。

#### 3\. WRY
[![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/921ad345c5f2417f9aeb8bf474775bbd~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)
](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Ftauri-apps%2Fwry "https://github.com/tauri-apps/wry")

> Rust中的跨平台`WebView渲染库`支持所有主要桌面平台，如Windows、macOS和Linux。
> 
> Wry连接每个平台上的web引擎，并提供易于使用和统一的界面来呈现WebView。它还将tao重新导出为事件循环和窗口创建的模块。

### 二、为什么推荐Tauri

#### 1\. 与Electron的技术选型比对

> 目前跨平台应用程序领域的领导者一直是`Electron`，它提供了`Nodejs`的后端和`Chromium`浏览器的前端，它将会产生一个非常大的可执行文件，这将会消耗大量内存。

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d597139f4340489690379bd2142da80c~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

> `Tauri`采用不同的方法，它用`Rust`的后端和`Tao`、`Wry`等库来提供轻量级的`webview`，最终的结果将是更小的包和更小的内存消耗。

![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d23633e68cba4101a0b0d6746f734597~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

#### 2\. 包体积大小比对

> `Tauri` 构建的桌面程序太小了，远不是`Electron`可以相比的，因为它放弃了体积巨大的`Chromium`内核和`nodejs`，而是选择了`webview`和 `Rust`。
> 
> 并且在内存使用率上来说，Tauri也是相当小的。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/57f8ac0df6cd4ea7abd949985f33e5e6~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

### 三、如何搭建一个Tauri应用程序

#### 1\. 前期环境准备

##### ① 需要安装CLang 和 macOS 开发依赖项

```bash
$ xcode-select --install

```

##### ② 安装 Rust 环境

```bash
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh

```

_该命令会下载一个脚本并开始安装该rustup工具，该工具会安装最新的稳定版 Rust。如果安装成功，将出现以下行：_

```bash
$ Rust is installed now. Great!

```

_可以通过查看Rust版本确认是否安装成功：_

```bash
$ rustc --version

```

_若是已安装过Rust，可使用下面命令升级版本_

```bash
$ rustup update

```

##### ③ 安装 Tauri-cli

> tauri-cli是开发过程的核心。它运行 Cargo 来编译 Rust 核心，启动前端#开发服务器，在构建生产时捆绑所有assets, sidecars and resources，甚至负责代码签名！

```bash
$ cargo install tauri-cli --version "^1.0.0"

```

_查看版本Tauri版本确认是否安装成功_

```bash
$ cargo tauri --version

```

#### 2\. 创建新项目并启动

##### ① 通过tauri-cli新建项目

```bash
$ yarn create tauri-app

```

**📢 此处需要注意 node >= 14**

_通过tauri-cli新建项目，一步步选择自己喜欢的前端框架来安装项目，安装过程如下图所示：_

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/7411aee60d9e433fbc8f64660b844a61~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

此处省略部分包安装过程......（直接看最后安装成功的样子）

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0fecba9452cf4f8ea2ce828993320567~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

##### ② 启动项目

```base
$ yarn tauri dev

```

_启动项目：首次启动tauri，Rust 包管理器会下载安装好多依赖，可能会比较耗时，第二次之后就会非常快，因为有缓存。_

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/cd94e3d4da7147cc98a91e5a2311f3b4~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

#### 3\. 现有项目中添加Tauri并启动

##### ① 创建一个React项目

```bash
$ npm init react-app tauri-react

```

##### ② 安装 tauri-cli 包作为开发依赖

```bash
$ npm install -D @tauri-apps/cli

```

##### ③ 安装 tauri-api 包安装为依赖项（可选）

_该包推荐用于使用 ES 模块或现代构建工具的项目。这是访问 Tauri API 的最安全方式。_

```bash
$ npm install @tauri-apps/api

```

##### ④ 初始化项目

```bash
$ npm run tauri init

```

初始化项目会在目录中生成 ./src-tauri

需确认以下配置项 ./src-tauri/tauri.conf.json，`devPath`是本地项目启动的路径

```json
"build": {
    "beforeBuildCommand": "npm run build",
    "beforeDevCommand": "npm run start",
    "devPath": "http://localhost:3000", 
    "distDir": "../build"
},

```

##### ⑤ 添加启动命令

_首先需要在 package.json 中添加一个自定义脚本_

```json
"scripts": {
    "tauri": "tauri"
}

```

##### ⑥ 启动项目

```bash
$ npm run tauri dev

```

#### 4\. 编译打包

```base
$ yarn tauri build

```

Tauri的打包，与Electron不同，Tauri只能生成当前操作系统对应的程序包。 ![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6d6461abf2ad45bd8f23f3a9bf2dfeb7~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

#### 5\. 项目结构目录

```json
├─ build
├─ node_modules
├─ public
├─ src                    
   ├─ App.css
   ├─ App.tsx
   ├─ favicon.svg
   ├─ index.css
   ├─ index.tsx
   ├─ logo.svg
   └─ main.tsx
├─ src-tauri             
   ├─ icons           
   ├─ src             
   ├─ target          
   ├─ Cargo.toml      
   ├─ build.rs        
   └─ tauri.conf.json 
├─ package.json           
├─ tsconfig.json
└─ yarn.lock

```

_也可以通过命令来查看Tauri项目的包安装情况_

```bash
$ npm run tauri info

```

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ae350cebaf4543929d7d8f3c0b97a964~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

#### 6\. tauri.conf.json配置介绍

> *   `tauri.conf.json` 由以下部分组成：
>     *   build：构建配置
>     *   package：Package 设置
>     *   [tauri](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23tauriconfig "https://tauri.app/v1/api/config/#tauriconfig")
>         *   [pattern](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23patternkind "https://tauri.app/v1/api/config/#patternkind") 选择使用模式
>         *   [windows](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23windowconfig "https://tauri.app/v1/api/config/#windowconfig") 窗口配置
>         *   [bundle](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23bundleconfig "https://tauri.app/v1/api/config/#bundleconfig") 捆绑器配置
>         *   [security](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23securityconfig "https://tauri.app/v1/api/config/#securityconfig") 安全模式
>         *   [updater](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23updaterconfig "https://tauri.app/v1/api/config/#updaterconfig") 更新应用配置，如签名公钥，更新应用的窗口配置等
>         *   [allowlist](https://link.juejin.cn/?target=https%3A%2F%2Ftauri.app%2Fv1%2Fapi%2Fconfig%2F%23allowlistconfig "https://tauri.app/v1/api/config/#allowlistconfig") 白名单配置，如系统文件，路径，脚本，进程等
> *   plugins：插件配置

```json

{
  "build": {
    "beforeBuildCommand": "yarn build",
    "beforeDevCommand": "yarn start",
    "devPath": "http://localhost:3000",
    "distDir": "../build"
  },
  "package": {
    "productName": "tauri-test-app",
    "version": "0.1.0"
  },
  "tauri": {
    "pattern": {
      "use": "brownfield"
    },
    "allowlist": {
      "all": true
    },
    "bundle": {},
    "security": {
      "csp": null
    },
    "updater": {
      "active": false
    },
    "windows": [
      {
        "fullscreen": false,
        "height": 900,
        "resizable": true,
        "title": "tauri-test-app",
        "width": 480
      }
    ]
  }
}

```

[源代码地址](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fliu-ningning%2Ftauri-app "https://github.com/liu-ningning/tauri-app")

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b06d70673f2249ca8d616e6a1b6fbabd~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp?)

欢迎喜欢钻研技术的小伙伴一起交流！