选择`KVM VPS`，注意，这里不要选`open VZ`的`VPS`，因为这个虚拟主机不能进行`bbr plus`加速。
之所以选择Ubuntu16位的系统是因为笔者试过了debian，centos的系统，发现都不行，真是所有坑都被我踩了。

输入下面命令回车，你可以复制过去，然后在 Xshell 界面按 Shift + Insert 即可粘贴，不能按 Ctrl + V 的。

```bash
bash <(curl -s -L https://git.io/v2ray.sh)
```

如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl

ubuntu/debian 系统安装 Curl 方法:

```bash
apt-get update -y && apt-get install curl -y
```

centos 系统安装 Curl 方法:

```bash
yum update -y && yum install curl -y
```

安装好 curl 之后就能安装脚本了![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221854.png)

输入1，回车，开始安装

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221822.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221822.png)

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221926.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221926.png)

选择协议，默认TCP，回车即可

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221935.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221935.png)

选择端口，回车

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221944.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031221944.png)

广告拦截，回车自动选择N

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222020.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222020.png)

配置Shadowsocks，有需要的可以配置，也可以先不配置，等配置好v2ray以后在配置也可以

最后按enter键，等待一会，会有v2ray的配置信息出现，说明配置好了

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222029.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222029.png)

下载v2ray的客户端，然后导入刚刚复制的复制的配置信息，客户端下载[传送门](https://github.com/2dust/v2rayN/releases/tag/2.50)

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222101.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222101.png)

选择从剪切板导入，导入成功后会出现下图

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222206.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222206.png)

有点右下角的v2ray客户端小图标，点击启用http代理

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222158.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222158.png)

模式选择，有**全局模式**和PAC模式，

**全局模式**状态下，你访问的所有流量都会先经过vps服务器，相当于vps是一个中间者，

**PAC模式**状态下，你访问的流量会自动分流，国内的网站不会经过vps，只有国外的网站才会经过vps

OK,现在就可以访问Google试试了，

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222226.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222226.png)

访问YouTube

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222556.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222556.png)

到这里，FQ已经是成功了，但是，有个问题就是访问的网速却很慢，so，需要进行加速操作。

## 4.1 安装证书
命令：
```bash
apt-get -y install ca-certificates
或
yum -y install ca-certificates
```
[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222739.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222739.png)

--------------------------------------
## 4.2 安装加速脚本

命令：

```plain
wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

先在\[1– 3\]切换内核（第一次显示为bbr内核也要切换一遍），重启

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222542.png)
安装完成，重启vps

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222834.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222834.png)

## 4.2 运行
重启后不用再下载脚本，直接`./tcp.sh` ，在\[4 – 8\]中选你要开的加速

> “1. 安装 BBR/BBR魔改版内核” 对应4,5,6（原版，魔改，暴力魔改）
> 
> “2. 安装 BBRplus版内核 ” 对应7（plus）
> 
> “3. 安装 Lotserver(锐速)内核” 对应8（锐速）

开启后再 ./tcp.sh ， 显示开启成功则启动成功，你也可以自己手动确认

现在你可以自由的切换你想要的加速，直到你不想折腾为止~
HostYun使用BBR魔改版
[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222842.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222842.png)

[![](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222848.png)
](https://madcoding-image.oss-cn-hongkong.aliyuncs.com/20191031222848.png)

然后在访问YouTube，测试速度，发现速度飕飕的。1080p点到哪里看哪里。

1.  [https://github.com/233boy/v2ray/wiki/V2Ray%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E5%9B%BE%E6%96%87%E6%95%99%E7%A8%8B](https://github.com/233boy/v2ray/wiki/V2Ray%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E5%9B%BE%E6%96%87%E6%95%99%E7%A8%8B)
2.  [https://zhujiwiki.com/8563/](https://zhujiwiki.com/8563/)