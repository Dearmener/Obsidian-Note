> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.vpsgo.com](https://www.vpsgo.com/about-163-cn2-gt-gia.html)

> CN2 是什么？CN2 GT 是什么？CN2 GIA 是什么？我们在选择国外 VPS 时经常会看到 163 骨干网、CN2 GT 线路、CN2 GIA 线路，其实 CN2 是电信的一种优化线路，今天 VPS GO 就介绍下三者的区别和联系，并推荐几家提供 CN2 GT 和 CN2 GIA 线路的 VPS 商家。

[CN2 是什么](https://www.vpsgo.com/tag/cn2%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2是什么的所有文章")？[CN2 GT 是什么](https://www.vpsgo.com/tag/cn2-gt%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2 GT是什么的所有文章")？[CN2 GIA 是什么](https://www.vpsgo.com/tag/cn2-gia%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2 GIA是什么的所有文章")？我们在选择国外 VPS 时经常会看到 [163 骨干网](https://www.vpsgo.com/tag/163%e9%aa%a8%e5%b9%b2%e7%bd%91 "查看163骨干网的所有文章")、[CN2 GT](https://www.vpsgo.com/tag/cn2-gt "查看CN2 GT的所有文章") 线路、[CN2 GIA](https://www.vpsgo.com/tag/cn2-gia "查看CN2 GIA的所有文章") 线路，其实 [CN2](https://www.vpsgo.com/tag/cn2 "查看CN2的所有文章") 是电信的一种优化线路，今天 [VPS GO](https://www.vpsgo.com/) 就介绍下三者的区别和联系，并推荐几家提供 CN2 GT 和 CN2 GIA 线路的 VPS 商家。

**一、基本概念**
----------

首先确定的是，[电信 CN2](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2 "查看电信CN2的所有文章") 优化线路（CN2 GT 和 CN2 GIA）都是针对电信的网络，如果是三网 CN2 的话是指移动和联通也会走电信的 CN2 线路，一般会在国内就跳到电信的 CN2 节点，然后再走国际出口，如此来享受 CN2 线路，所以有了 “[三网 CN2 GIA](https://www.vpsgo.com/tag/%e4%b8%89%e7%bd%91cn2-gia "查看三网CN2 GIA的所有文章")” 的说法。

CN2，全称是中国电信下一代承载网（Chinatelecom Next Carrier Network，CNCN），再对 CNCN 缩写，就得到了 CN2，CN2 作为 “精品网络项目” 被电信推出，线路质量肯定比传统 163 骨干网好。

目前，电信国际出口一般有 3 种承载网络类型，包括传统 163 骨干网，CN2 GT 线路和 CN2 GIA 线路：

1.  **传统 163 骨干网**：这是最常见也是最普通的线路，也叫 [ChinaNet](https://www.vpsgo.com/tag/chinanet "查看ChinaNet的所有文章")(AS4134)，没有针对电信用户优化的线路一般走的就是这个承载网络类型（全程 202.97 节点），因为用的人多，线路也没有优化，所以在晚高峰会出现线路卡顿，以及丢包率高的情况。
2.  **CN2 GT 线路**：GT 是 Global Transit 的缩写，CN2 GT 也是 CN2 线路的一种，但是是 CN2 线路中的中端产品，在 CN2 里的等级比较低，去程和回程都会有 202.97 传统节点的出现，一般来说是 202.97 和 59.43 两种节点都会出现，并且只有在国际出口才会走 59.43 CN2 节点。CN2 GT 线路因为加入了 59.43 高速节点，CN2(AS4809)，线路质量会比传统 163 骨干网优秀。
3.  **CN2 GIA 线路**：GIA 是 Global Internet Access 的缩写，CN2 GIA 自然也是 CN2 线路的一种，并且是 CN2 线路中的高端产品，在 CN2 里的等级最高，去程和回程全部走 59.43 高速节点，CN2(AS4809)。CN2 GIA 线路一般比较稳定，速度快，丢包率低。

CN2 一般是指电信 CN2，同理可以解释[电信 CN2 GT](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gt "查看电信CN2 GT的所有文章")、[电信 CN2 GIA](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gia "查看电信CN2 GIA的所有文章")，而三网 CN2 GIA 则是指移动和联通也会使用电信 CN2 节点连接国际网络，相关概念介绍

*   《[CN2 对移动和联通有优化吗？什么是移动 / 联通 / 三网 CN2 GIA？](https://www.vpsgo.com/cn2-gia-to-chinamobile-chinaunicom.html)》
*   《[什么是去程 CN2 GIA？什么是回程 CN2 GIA？什么是双向 CN2 GIA？](https://www.vpsgo.com/cn2-gia-route.html)》

**二、区别对比**
----------

要说 163 骨干网、CN2 GT 线路和 CN2 GIA 线路之间的区别，就不得不讲 [QoS](https://www.vpsgo.com/tag/qos "查看QoS的所有文章")（Quality of Service，服务质量）技术。

QoS 是一种控制机制，它提供了针对不同用户或者不同数据流采用相应不同的优先级，通俗一点讲，到了晚高峰，很多人抢着一起用国际出口的带宽，QoS 就通过控制，让线路级别高的用户（政府用户 / 企业用户 / CN2 线路）先出去，而传统 163 骨干网可能优先级不够甚至会被直接丢弃，于是就出现了丢包率高的情况。

因此，163 骨干网和 CN2 优化线路的**最明显的区别**就是，前者属于可能被 QoS 的普通线路，而后者则是有优先出口权限的优化线路，而我们用起来的直观感受就是 CN2 线路相比于 163 骨干网更加的稳定，更快，丢包率低。

**三、CN2 判断**
------------

之前已经介绍了传统 163 骨干网，CN2 GT 线路和 CN2 GIA 线路的基本概念，这一部分就介绍下 [CN2 GIA 判断](https://www.vpsgo.com/tag/cn2-gia%e5%88%a4%e6%96%ad "查看CN2 GIA判断的所有文章")方法，如何测试你的 VPS 线路是不是 CN2 GT/CN2 GIA 优化。

其实 [CN2 GIA 测试](https://www.vpsgo.com/tag/cn2-gia%e6%b5%8b%e8%af%95 "查看CN2 GIA测试的所有文章")方法很简单，就是看回程路由和去程路由里的节点类型，看路由里走的 202.97 普通节点还是 59.43 高速节点。

**去程路由判断**就直接有 traceroute 在线工具（地址：https://tools.ipip.net/traceroute.php）测试即可，以下面的搬瓦工 CN2GIA>本文由[简悦SimpRead](http://ksria.com/simpread/)转码，原文地址[www.vpsgo.com](https://www.vpsgo.com/about-163-cn2-gt-gia.html)

>CN2是什么？CN2GT是什么？CN2GIA是什么？我们在选择国外VPS时经常会看到163骨干网、CN2GT线路、CN2GIA线路，其实CN2是电信的一种优化线路，今天VPSGO就介绍下三者的区别和联系，并推荐几家提供CN2GT和CN2GIA线路的VPS商家。

[CN2是什么](https://www.vpsgo.com/tag/cn2%e6%98%af%e4%bb%80%e4%b9%88"查看CN2是什么的所有文章")？[CN2GT是什么](https://www.vpsgo.com/tag/cn2-gt%e6%98%af%e4%bb%80%e4%b9%88"查看CN2GT是什么的所有文章")？[CN2GIA是什么](https://www.vpsgo.com/tag/cn2-gia%e6%98%af%e4%bb%80%e4%b9%88"查看CN2GIA是什么的所有文章")？我们在选择国外VPS时经常会看到[163骨干网](https://www.vpsgo.com/tag/163%e9%aa%a8%e5%b9%b2%e7%bd%91"查看163骨干网的所有文章")、[CN2GT](https://www.vpsgo.com/tag/cn2-gt"查看CN2GT的所有文章")线路、[CN2GIA](https://www.vpsgo.com/tag/cn2-gia"查看CN2GIA的所有文章")线路，其实[CN2](https://www.vpsgo.com/tag/cn2"查看CN2的所有文章")是电信的一种优化线路，今天[VPSGO](https://www.vpsgo.com/)就介绍下三者的区别和联系，并推荐几家提供CN2GT和CN2GIA线路的VPS商家。

**一、基本概念**
----------

首先确定的是，[电信CN2](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2"查看电信CN2的所有文章")优化线路（CN2GT和CN2GIA）都是针对电信的网络，如果是三网CN2的话是指移动和联通也会走电信的CN2线路，一般会在国内就跳到电信的CN2节点，然后再走国际出口，如此来享受CN2线路，所以有了“[三网CN2GIA](https://www.vpsgo.com/tag/%e4%b8%89%e7%bd%91cn2-gia"查看三网CN2GIA的所有文章")”的说法。

CN2，全称是中国电信下一代承载网（ChinatelecomNextCarrierNetwork，CNCN），再对CNCN缩写，就得到了CN2，CN2作为“精品网络项目”被电信推出，线路质量肯定比传统163骨干网好。

目前，电信国际出口一般有3种承载网络类型，包括传统163骨干网，CN2GT线路和CN2GIA线路：

1.**传统163骨干网**：这是最常见也是最普通的线路，也叫[ChinaNet](https://www.vpsgo.com/tag/chinanet"查看ChinaNet的所有文章")(AS4134)，没有针对电信用户优化的线路一般走的就是这个承载网络类型（全程202.97节点），因为用的人多，线路也没有优化，所以在晚高峰会出现线路卡顿，以及丢包率高的情况。
2.**CN2GT线路**：GT是GlobalTransit的缩写，CN2GT也是CN2线路的一种，但是是CN2线路中的中端产品，在CN2里的等级比较低，去程和回程都会有202.97传统节点的出现，一般来说是202.97和59.43两种节点都会出现，并且只有在国际出口才会走59.43CN2节点。CN2GT线路因为加入了59.43高速节点，CN2(AS4809)，线路质量会比传统163骨干网优秀。
3.**CN2GIA线路**：GIA是GlobalInternetAccess的缩写，CN2GIA自然也是CN2线路的一种，并且是CN2线路中的高端产品，在CN2里的等级最高，去程和回程全部走59.43高速节点，CN2(AS4809)。CN2GIA线路一般比较稳定，速度快，丢包率低。

CN2一般是指电信CN2，同理可以解释[电信CN2GT](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gt"查看电信CN2GT的所有文章")、[电信CN2GIA](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gia"查看电信CN2GIA的所有文章")，而三网CN2GIA则是指移动和联通也会使用电信CN2节点连接国际网络，相关概念介绍

*《[CN2对移动和联通有优化吗？什么是移动/联通/三网CN2GIA？](https://www.vpsgo.com/cn2-gia-to-chinamobile-chinaunicom.html)》
*《[什么是去程CN2GIA？什么是回程CN2GIA？什么是双向CN2GIA？](https://www.vpsgo.com/cn2-gia-route.html)》

**二、区别对比**
----------

要说163骨干网、CN2GT线路和CN2GIA线路之间的区别，就不得不讲[QoS](https://www.vpsgo.com/tag/qos"查看QoS的所有文章")（QualityofService，服务质量）技术。

QoS是一种控制机制，它提供了针对不同用户或者不同数据流采用相应不同的优先级，通俗一点讲，到了晚高峰，很多人抢着一起用国际出口的带宽，QoS就通过控制，让线路级别高的用户（政府用户/企业用户/CN2线路）先出去，而传统163骨干网可能优先级不够甚至会被直接丢弃，于是就出现了丢包率高的情况。

因此，163骨干网和CN2优化线路的**最明显的区别**就是，前者属于可能被QoS的普通线路，而后者则是有优先出口权限的优化线路，而我们用起来的直观感受就是CN2线路相比于163骨干网更加的稳定，更快，丢包率低。

**三、CN2判断**
------------

之前已经介绍了传统163骨干网，CN2GT线路和CN2GIA线路的基本概念，这一部分就介绍下[CN2GIA判断](https://www.vpsgo.com/tag/cn2-gia%e5%88%a4%e6%96%ad"查看CN2GIA判断的所有文章")方法，如何测试你的VPS线路是不是CN2GT/CN2GIA优化。

其实[CN2GIA测试](https://www.vpsgo.com/tag/cn2-gia%e6%b5%8b%e8%af%95"查看CN2GIA测试的所有文章")方法很简单，就是看回程路由和去程路由里的节点类型，看路由里走的202.97普通节点还是59.43高速节点。

**去程路由判断**就直接有traceroute在线工具（地址：https://tools.ipip.net/traceroute.php）测试即可，以下面的搬瓦工CN2GIA为例，省级出口以上都是59.43高速节点，因此是CN2GIA类型：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-traceroute.png)

**回程路线判断**则需要自己的VPS上借助mtr工具，执行命令`mtr-rwip`查看回程路由，依然以搬瓦工的CN2GIA线路为例（依然保证省级出口以上都是59.43高速节点）：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-mtr.png)

作为参考，再放一张CN2GT线路的去程路由，可以看到202.97普通节点的数量明显增多，从南京电信->上海电信依然是202.97节点：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-traceroute.png)

同理，如果是163骨干网，那么全程都是202.97普通节点。

163骨干网和CN2线路的区别很明显，但是CN2GT线路和CN2GIA线路都走了59.43和202.97节点，那么应该如何[区分CN2GT和CN2GIA](https://www.vpsgo.com/tag/%e5%8c%ba%e5%88%86cn2-gt%e5%92%8ccn2-gia"查看区分CN2GT和CN2GIA的所有文章")呢？

*CN2GT和CN2GIA都保证国家与国家之间的传输在CN2骨干网（59.43节点）上进行，即国际出口走59.43；
*CN2GT的省级出口为202.97节点，只有在国际出口时才会走59.43，对比上述两张图可以看到，从南京电信->上海电信，CN2GT是202.97，而CN2GIA则已经走59.43了；
*CN2GIA线路如果本省有CN2节点，则直接接入该CN2节点。依然从上述两个例子，从江苏南通开始，本省有CN2节点（江苏南京），所以CN2GIA线路直接在江苏南京接上了CN2节点（59.43），之后就是从上海出口；
*CN2GIA线路如果本省没有CN2节点，则就近接入北上广的202.97节点，再接入该地的59.43节点。如图所示，从安徽芜湖电信先接入上海202.97，再到59.43，最后出口；

![](https://www.vpsgo.com/wp-content/uploads/2019/02/wuhu-cn2-gia.jpeg)

*CN2GIA如果在CN2节点城市，则直接走CN2节点（59.43），而CN2GT则会先走202.97，只有在国际出口处才会走59.43。如下图所示，在南京直接接入了59.43高速节点。（截止目前，包括但不限于以下城市已经有CN2节点：成都，南京，西安，武汉，乌鲁木齐，广州，上海，北京）

![](https://www.vpsgo.com/wp-content/uploads/2019/02/nanjing-cn2-gia.jpeg)

*综上，区分CN2GT和CN2GIA最简单的方法就是在有CN2节点的城市（如南京）跑去程路由，经过202.97的就是CN2GT，直接59.43的就是CN2GIA。

**四、CN2VPS推荐**
----------------

CN2GIA的线路更稳、速度更快，所以[CN2GIA价格](https://www.vpsgo.com/tag/cn2-gia%e4%bb%b7%e6%a0%bc"查看CN2GIA价格的所有文章")也会相对比较高。VPSGO已经做了关于CN2GIAVPS的详细推荐，系列文章如下：

*《[美国CN2GIAVPS服务器商家整理和推荐](https://www.vpsgo.com/usa-cn2-gia-vps.html)》
*《[香港CN2GIAVPS服务器商家整理和推荐](https://www.vpsgo.com/hong-kong-cn2-gia-vps.html)》

下面推荐几家靠谱的提供CN2线路的VPS商家。

**1、搬瓦工（BandWagonHost）（推荐）**

搬瓦工同时提供CN2GT线路和CN2GIA线路，机房在美国洛杉矶，带宽是1Gbps，KVM虚拟，同时，搬瓦工提供电子商务优化版的CN2GIA（搬瓦工DC6CN2GIA，CN2GIAECOMMERCE），最高提供10Gbps带宽。

搬瓦工优惠码：[BWH3HYATVBJW](https://bwh81.net/aff.php?aff=55247"点击复制")

搬瓦工DC6CN2GIA（CN2GIAECOMMERCE），走的Zenlayer（C3机房）的CN2GIA+Hivelocity，商务优化，最高可提供10Gbps带宽，方案汇总如下：

搬瓦工CN2GT线路电信走CN2GT，移动部分地区走CN2GT，部分走自己的线路，联通则是直连线路，方案汇总如下：

搬瓦工CN2GIA线路是电信/移动/联通三网都走CN2GIA，方案汇总如下（目前便宜方案没有货）：

更多搬瓦工教程整理：《[搬瓦工VPS专题：搬瓦工优惠码和搬瓦工新手教程整理](https://www.vpsgo.com/bandwagonhost.html)》

**2、HostDareCN2GIA**

HostDare的KVM方案电信CN2GIA，移动联通直连，同时HostDare提供大硬盘服务器，最高450G硬盘容量，并且4G内存以上的方案可以提供Windows服务器，方案汇总如下（优惠码：[HostDare优惠码：终身75折优惠/电信CN2GIA/移动联通直连](https://www.vpsgo.com/hostdare-75-promotion-code.html))

**3、GigsGigsCloudCN2GIA**

GigsGigsCloud推出的美西CN2GIA线路（洛杉矶机房），也是1Gbps的带宽，KVM虚拟，并且1G内存以上方案提供美国原生IP，电信/移动/联通三网直连，方案汇总如下（选择USSimpleCloudV）：

**4、DMITCN2GIA**

DMIT收购了HKSS的[洛杉矶CN2GIA](https://www.vpsgo.com/tag/%e6%b4%9b%e6%9d%89%e7%9f%b6cn2-gia"查看洛杉矶CN2GIA的所有文章")，现在无论是硬件实力还是客户群体上都有了质的飞跃，并且DMIT美西CN2GIA的优势是提供美国原生IP，可以解锁Netflix等流媒体。

**5、iONCloudCN2GT**

iON服务器的速度不错，隶属于老牌商家Krypt，也是很靠谱的一个商家，提供洛杉矶CN2GT线路，价格还比较适中，稳定性不错，方案整理如下：

**6、CN2GIA推荐整理**

VPSGO建议大家选择搬瓦工CN2GIA-E，稳定性和商家实力都没话说，老王有4台他家的CN2GIA方案，非常不错。演示网站：

1.搬瓦工DC6CN2GIA：[https://dc6.bwg.wiki](https://dc6.bwg.wiki/)
2.搬瓦工DC9CN2GIA：[https://dc9.bwg.wiki](https://dc9.bwg.wiki/)> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.vpsgo.com](https://www.vpsgo.com/about-163-cn2-gt-gia.html)

> CN2 是什么？CN2 GT 是什么？CN2 GIA 是什么？我们在选择国外 VPS 时经常会看到 163 骨干网、CN2 GT 线路、CN2 GIA 线路，其实 CN2 是电信的一种优化线路，今天 VPS GO 就介绍下三者的区别和联系，并推荐几家提供 CN2 GT 和 CN2 GIA 线路的 VPS 商家。

[CN2 是什么](https://www.vpsgo.com/tag/cn2%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2是什么的所有文章")？[CN2 GT 是什么](https://www.vpsgo.com/tag/cn2-gt%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2 GT是什么的所有文章")？[CN2 GIA 是什么](https://www.vpsgo.com/tag/cn2-gia%e6%98%af%e4%bb%80%e4%b9%88 "查看CN2 GIA是什么的所有文章")？我们在选择国外 VPS 时经常会看到 [163 骨干网](https://www.vpsgo.com/tag/163%e9%aa%a8%e5%b9%b2%e7%bd%91 "查看163骨干网的所有文章")、[CN2 GT](https://www.vpsgo.com/tag/cn2-gt "查看CN2 GT的所有文章") 线路、[CN2 GIA](https://www.vpsgo.com/tag/cn2-gia "查看CN2 GIA的所有文章") 线路，其实 [CN2](https://www.vpsgo.com/tag/cn2 "查看CN2的所有文章") 是电信的一种优化线路，今天 [VPS GO](https://www.vpsgo.com/) 就介绍下三者的区别和联系，并推荐几家提供 CN2 GT 和 CN2 GIA 线路的 VPS 商家。

**一、基本概念**
----------

首先确定的是，[电信 CN2](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2 "查看电信CN2的所有文章") 优化线路（CN2 GT 和 CN2 GIA）都是针对电信的网络，如果是三网 CN2 的话是指移动和联通也会走电信的 CN2 线路，一般会在国内就跳到电信的 CN2 节点，然后再走国际出口，如此来享受 CN2 线路，所以有了 “[三网 CN2 GIA](https://www.vpsgo.com/tag/%e4%b8%89%e7%bd%91cn2-gia "查看三网CN2 GIA的所有文章")” 的说法。

CN2，全称是中国电信下一代承载网（Chinatelecom Next Carrier Network，CNCN），再对 CNCN 缩写，就得到了 CN2，CN2 作为 “精品网络项目” 被电信推出，线路质量肯定比传统 163 骨干网好。

目前，电信国际出口一般有 3 种承载网络类型，包括传统 163 骨干网，CN2 GT 线路和 CN2 GIA 线路：

1.  **传统 163 骨干网**：这是最常见也是最普通的线路，也叫 [ChinaNet](https://www.vpsgo.com/tag/chinanet "查看ChinaNet的所有文章")(AS4134)，没有针对电信用户优化的线路一般走的就是这个承载网络类型（全程 202.97 节点），因为用的人多，线路也没有优化，所以在晚高峰会出现线路卡顿，以及丢包率高的情况。
2.  **CN2 GT 线路**：GT 是 Global Transit 的缩写，CN2 GT 也是 CN2 线路的一种，但是是 CN2 线路中的中端产品，在 CN2 里的等级比较低，去程和回程都会有 202.97 传统节点的出现，一般来说是 202.97 和 59.43 两种节点都会出现，并且只有在国际出口才会走 59.43 CN2 节点。CN2 GT 线路因为加入了 59.43 高速节点，CN2(AS4809)，线路质量会比传统 163 骨干网优秀。
3.  **CN2 GIA 线路**：GIA 是 Global Internet Access 的缩写，CN2 GIA 自然也是 CN2 线路的一种，并且是 CN2 线路中的高端产品，在 CN2 里的等级最高，去程和回程全部走 59.43 高速节点，CN2(AS4809)。CN2 GIA 线路一般比较稳定，速度快，丢包率低。

CN2 一般是指电信 CN2，同理可以解释[电信 CN2 GT](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gt "查看电信CN2 GT的所有文章")、[电信 CN2 GIA](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gia "查看电信CN2 GIA的所有文章")，而三网 CN2 GIA 则是指移动和联通也会使用电信 CN2 节点连接国际网络，相关概念介绍

*   《[CN2 对移动和联通有优化吗？什么是移动 / 联通 / 三网 CN2 GIA？](https://www.vpsgo.com/cn2-gia-to-chinamobile-chinaunicom.html)》
*   《[什么是去程 CN2 GIA？什么是回程 CN2 GIA？什么是双向 CN2 GIA？](https://www.vpsgo.com/cn2-gia-route.html)》

**二、区别对比**
----------

要说 163 骨干网、CN2 GT 线路和 CN2 GIA 线路之间的区别，就不得不讲 [QoS](https://www.vpsgo.com/tag/qos "查看QoS的所有文章")（Quality of Service，服务质量）技术。

QoS 是一种控制机制，它提供了针对不同用户或者不同数据流采用相应不同的优先级，通俗一点讲，到了晚高峰，很多人抢着一起用国际出口的带宽，QoS 就通过控制，让线路级别高的用户（政府用户 / 企业用户 / CN2 线路）先出去，而传统 163 骨干网可能优先级不够甚至会被直接丢弃，于是就出现了丢包率高的情况。

因此，163 骨干网和 CN2 优化线路的**最明显的区别**就是，前者属于可能被 QoS 的普通线路，而后者则是有优先出口权限的优化线路，而我们用起来的直观感受就是 CN2 线路相比于 163 骨干网更加的稳定，更快，丢包率低。

**三、CN2 判断**
------------

之前已经介绍了传统 163 骨干网，CN2 GT 线路和 CN2 GIA 线路的基本概念，这一部分就介绍下 [CN2 GIA 判断](https://www.vpsgo.com/tag/cn2-gia%e5%88%a4%e6%96%ad "查看CN2 GIA判断的所有文章")方法，如何测试你的 VPS 线路是不是 CN2 GT/CN2 GIA 优化。

其实 [CN2 GIA 测试](https://www.vpsgo.com/tag/cn2-gia%e6%b5%8b%e8%af%95 "查看CN2 GIA测试的所有文章")方法很简单，就是看回程路由和去程路由里的节点类型，看路由里走的 202.97 普通节点还是 59.43 高速节点。

**去程路由判断**就直接有 traceroute 在线工具（地址：https://tools.ipip.net/traceroute.php）测试即可，以下面的搬瓦工 CN2GIA>本文由[简悦SimpRead](http://ksria.com/simpread/)转码，原文地址[www.vpsgo.com](https://www.vpsgo.com/about-163-cn2-gt-gia.html)

>CN2是什么？CN2GT是什么？CN2GIA是什么？我们在选择国外VPS时经常会看到163骨干网、CN2GT线路、CN2GIA线路，其实CN2是电信的一种优化线路，今天VPSGO就介绍下三者的区别和联系，并推荐几家提供CN2GT和CN2GIA线路的VPS商家。

[CN2是什么](https://www.vpsgo.com/tag/cn2%e6%98%af%e4%bb%80%e4%b9%88"查看CN2是什么的所有文章")？[CN2GT是什么](https://www.vpsgo.com/tag/cn2-gt%e6%98%af%e4%bb%80%e4%b9%88"查看CN2GT是什么的所有文章")？[CN2GIA是什么](https://www.vpsgo.com/tag/cn2-gia%e6%98%af%e4%bb%80%e4%b9%88"查看CN2GIA是什么的所有文章")？我们在选择国外VPS时经常会看到[163骨干网](https://www.vpsgo.com/tag/163%e9%aa%a8%e5%b9%b2%e7%bd%91"查看163骨干网的所有文章")、[CN2GT](https://www.vpsgo.com/tag/cn2-gt"查看CN2GT的所有文章")线路、[CN2GIA](https://www.vpsgo.com/tag/cn2-gia"查看CN2GIA的所有文章")线路，其实[CN2](https://www.vpsgo.com/tag/cn2"查看CN2的所有文章")是电信的一种优化线路，今天[VPSGO](https://www.vpsgo.com/)就介绍下三者的区别和联系，并推荐几家提供CN2GT和CN2GIA线路的VPS商家。

**一、基本概念**
----------

首先确定的是，[电信CN2](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2"查看电信CN2的所有文章")优化线路（CN2GT和CN2GIA）都是针对电信的网络，如果是三网CN2的话是指移动和联通也会走电信的CN2线路，一般会在国内就跳到电信的CN2节点，然后再走国际出口，如此来享受CN2线路，所以有了“[三网CN2GIA](https://www.vpsgo.com/tag/%e4%b8%89%e7%bd%91cn2-gia"查看三网CN2GIA的所有文章")”的说法。

CN2，全称是中国电信下一代承载网（ChinatelecomNextCarrierNetwork，CNCN），再对CNCN缩写，就得到了CN2，CN2作为“精品网络项目”被电信推出，线路质量肯定比传统163骨干网好。

目前，电信国际出口一般有3种承载网络类型，包括传统163骨干网，CN2GT线路和CN2GIA线路：

1.**传统163骨干网**：这是最常见也是最普通的线路，也叫[ChinaNet](https://www.vpsgo.com/tag/chinanet"查看ChinaNet的所有文章")(AS4134)，没有针对电信用户优化的线路一般走的就是这个承载网络类型（全程202.97节点），因为用的人多，线路也没有优化，所以在晚高峰会出现线路卡顿，以及丢包率高的情况。
2.**CN2GT线路**：GT是GlobalTransit的缩写，CN2GT也是CN2线路的一种，但是是CN2线路中的中端产品，在CN2里的等级比较低，去程和回程都会有202.97传统节点的出现，一般来说是202.97和59.43两种节点都会出现，并且只有在国际出口才会走59.43CN2节点。CN2GT线路因为加入了59.43高速节点，CN2(AS4809)，线路质量会比传统163骨干网优秀。
3.**CN2GIA线路**：GIA是GlobalInternetAccess的缩写，CN2GIA自然也是CN2线路的一种，并且是CN2线路中的高端产品，在CN2里的等级最高，去程和回程全部走59.43高速节点，CN2(AS4809)。CN2GIA线路一般比较稳定，速度快，丢包率低。

CN2一般是指电信CN2，同理可以解释[电信CN2GT](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gt"查看电信CN2GT的所有文章")、[电信CN2GIA](https://www.vpsgo.com/tag/%e7%94%b5%e4%bf%a1cn2-gia"查看电信CN2GIA的所有文章")，而三网CN2GIA则是指移动和联通也会使用电信CN2节点连接国际网络，相关概念介绍

*《[CN2对移动和联通有优化吗？什么是移动/联通/三网CN2GIA？](https://www.vpsgo.com/cn2-gia-to-chinamobile-chinaunicom.html)》
*《[什么是去程CN2GIA？什么是回程CN2GIA？什么是双向CN2GIA？](https://www.vpsgo.com/cn2-gia-route.html)》

**二、区别对比**
----------

要说163骨干网、CN2GT线路和CN2GIA线路之间的区别，就不得不讲[QoS](https://www.vpsgo.com/tag/qos"查看QoS的所有文章")（QualityofService，服务质量）技术。

QoS是一种控制机制，它提供了针对不同用户或者不同数据流采用相应不同的优先级，通俗一点讲，到了晚高峰，很多人抢着一起用国际出口的带宽，QoS就通过控制，让线路级别高的用户（政府用户/企业用户/CN2线路）先出去，而传统163骨干网可能优先级不够甚至会被直接丢弃，于是就出现了丢包率高的情况。

因此，163骨干网和CN2优化线路的**最明显的区别**就是，前者属于可能被QoS的普通线路，而后者则是有优先出口权限的优化线路，而我们用起来的直观感受就是CN2线路相比于163骨干网更加的稳定，更快，丢包率低。

**三、CN2判断**
------------

之前已经介绍了传统163骨干网，CN2GT线路和CN2GIA线路的基本概念，这一部分就介绍下[CN2GIA判断](https://www.vpsgo.com/tag/cn2-gia%e5%88%a4%e6%96%ad"查看CN2GIA判断的所有文章")方法，如何测试你的VPS线路是不是CN2GT/CN2GIA优化。

其实[CN2GIA测试](https://www.vpsgo.com/tag/cn2-gia%e6%b5%8b%e8%af%95"查看CN2GIA测试的所有文章")方法很简单，就是看回程路由和去程路由里的节点类型，看路由里走的202.97普通节点还是59.43高速节点。

**去程路由判断**就直接有traceroute在线工具（地址：https://tools.ipip.net/traceroute.php）测试即可，以下面的搬瓦工CN2GIA为例，省级出口以上都是59.43高速节点，因此是CN2GIA类型：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-traceroute.png)

**回程路线判断**则需要自己的VPS上借助mtr工具，执行命令`mtr-rwip`查看回程路由，依然以搬瓦工的CN2GIA线路为例（依然保证省级出口以上都是59.43高速节点）：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-mtr.png)

作为参考，再放一张CN2GT线路的去程路由，可以看到202.97普通节点的数量明显增多，从南京电信->上海电信依然是202.97节点：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-traceroute.png)

同理，如果是163骨干网，那么全程都是202.97普通节点。

163骨干网和CN2线路的区别很明显，但是CN2GT线路和CN2GIA线路都走了59.43和202.97节点，那么应该如何[区分CN2GT和CN2GIA](https://www.vpsgo.com/tag/%e5%8c%ba%e5%88%86cn2-gt%e5%92%8ccn2-gia"查看区分CN2GT和CN2GIA的所有文章")呢？

*CN2GT和CN2GIA都保证国家与国家之间的传输在CN2骨干网（59.43节点）上进行，即国际出口走59.43；
*CN2GT的省级出口为202.97节点，只有在国际出口时才会走59.43，对比上述两张图可以看到，从南京电信->上海电信，CN2GT是202.97，而CN2GIA则已经走59.43了；
*CN2GIA线路如果本省有CN2节点，则直接接入该CN2节点。依然从上述两个例子，从江苏南通开始，本省有CN2节点（江苏南京），所以CN2GIA线路直接在江苏南京接上了CN2节点（59.43），之后就是从上海出口；
*CN2GIA线路如果本省没有CN2节点，则就近接入北上广的202.97节点，再接入该地的59.43节点。如图所示，从安徽芜湖电信先接入上海202.97，再到59.43，最后出口；

![](https://www.vpsgo.com/wp-content/uploads/2019/02/wuhu-cn2-gia.jpeg)

*CN2GIA如果在CN2节点城市，则直接走CN2节点（59.43），而CN2GT则会先走202.97，只有在国际出口处才会走59.43。如下图所示，在南京直接接入了59.43高速节点。（截止目前，包括但不限于以下城市已经有CN2节点：成都，南京，西安，武汉，乌鲁木齐，广州，上海，北京）

![](https://www.vpsgo.com/wp-content/uploads/2019/02/nanjing-cn2-gia.jpeg)

*综上，区分CN2GT和CN2GIA最简单的方法就是在有CN2节点的城市（如南京）跑去程路由，经过202.97的就是CN2GT，直接59.43的就是CN2GIA。

**四、CN2VPS推荐**
----------------

CN2GIA的线路更稳、速度更快，所以[CN2GIA价格](https://www.vpsgo.com/tag/cn2-gia%e4%bb%b7%e6%a0%bc"查看CN2GIA价格的所有文章")也会相对比较高。VPSGO已经做了关于CN2GIAVPS的详细推荐，系列文章如下：

*《[美国CN2GIAVPS服务器商家整理和推荐](https://www.vpsgo.com/usa-cn2-gia-vps.html)》
《[香港CN2GIAVPS服务器商家整理和推荐](https://www.vpsgo.com/hong-kong-cn2-gia-vps.html)》

下面推荐几家靠谱的提供CN2线路的VPS商家。

**1、搬瓦工（BandWagonHost）（推荐）**

搬瓦工同时提供CN2GT线路和CN2GIA线路，机房在美国洛杉矶，带宽是1Gbps，KVM虚拟，同时，搬瓦工提供电子商务优化版的CN2GIA（搬瓦工DC6CN2GIA，CN2GIAECOMMERCE），最高提供10Gbps带宽。

搬瓦工优惠码：[BWH3HYATVBJW](https://bwh81.net/aff.php?aff=55247"点击复制")

搬瓦工DC6CN2GIA（CN2GIAECOMMERCE），走的Zenlayer（C3机房）的CN2GIA+Hivelocity，商务优化，最高可提供10Gbps带宽，方案汇总如下：

搬瓦工CN2GT线路电信走CN2GT，移动部分地区走CN2GT，部分走自己的线路，联通则是直连线路，方案汇总如下：

搬瓦工CN2GIA线路是电信/移动/联通三网都走CN2GIA，方案汇总如下（目前便宜方案没有货）：

更多搬瓦工教程整理：《[搬瓦工VPS专题：搬瓦工优惠码和搬瓦工新手教程整理](https://www.vpsgo.com/bandwagonhost.html)》

**2、HostDareCN2GIA**

HostDare的KVM方案电信CN2GIA，移动联通直连，同时HostDare提供大硬盘服务器，最高450G硬盘容量，并且4G内存以上的方案可以提供Windows服务器，方案汇总如下（优惠码：[HostDare优惠码：终身75折优惠/电信CN2GIA/移动联通直连](https://www.vpsgo.com/hostdare-75-promotion-code.html))

**3、GigsGigsCloudCN2GIA**

GigsGigsCloud推出的美西CN2GIA线路（洛杉矶机房），也是1Gbps的带宽，KVM虚拟，并且1G内存以上方案提供美国原生IP，电信/移动/联通三网直连，方案汇总如下（选择USSimpleCloudV）：

**4、DMITCN2GIA**

DMIT收购了HKSS的[洛杉矶CN2GIA](https://www.vpsgo.com/tag/%e6%b4%9b%e6%9d%89%e7%9f%b6cn2-gia"查看洛杉矶CN2GIA的所有文章")，现在无论是硬件实力还是客户群体上都有了质的飞跃，并且DMIT美西CN2GIA的优势是提供美国原生IP，可以解锁Netflix等流媒体。

**5、iONCloudCN2GT**

iON服务器的速度不错，隶属于老牌商家Krypt，也是很靠谱的一个商家，提供洛杉矶CN2GT线路，价格还比较适中，稳定性不错，方案整理如下：

**6、CN2GIA推荐整理**

VPSGO建议大家选择搬瓦工CN2GIA-E，稳定性和商家实力都没话说，老王有4台他家的CN2GIA方案，非常不错。演示网站：

1.搬瓦工DC6CN2GIA：[https://dc6.bwg.wiki](https://dc6.bwg.wiki/)
2.搬瓦工DC9CN2GIA：[https://dc9.bwg.wiki](https://dc9.bwg.wiki/) 为例，省级出口以上都是 59.43 高速节点，因此是 CN2 GIA 类型：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-traceroute.png)

**回程路线判断**则需要自己的 VPS 上借助 mtr 工具，执行命令`mtr -rw ip`查看回程路由，依然以搬瓦工的 CN2 GIA 线路为例（依然保证省级出口以上都是 59.43 高速节点）：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-mtr.png)

作为参考，再放一张 CN2 GT 线路的去程路由，可以看到 202.97 普通节点的数量明显增多，从南京电信 -> 上海电信依然是 202.97 节点：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-traceroute.png)

同理，如果是 163 骨干网，那么全程都是 202.97 普通节点。

163 骨干网和 CN2 线路的区别很明显，但是 CN2 GT 线路和 CN2 GIA 线路都走了 59.43 和 202.97 节点，那么应该如何[区分 CN2 GT 和 CN2 GIA](https://www.vpsgo.com/tag/%e5%8c%ba%e5%88%86cn2-gt%e5%92%8ccn2-gia "查看区分CN2 GT和CN2 GIA的所有文章") 呢？

*   CN2 GT 和 CN2 GIA 都保证国家与国家之间的传输在 CN2 骨干网（59.43 节点）上进行，即国际出口走 59.43；
*   CN2 GT 的省级出口为 202.97 节点，只有在国际出口时才会走 59.43，对比上述两张图可以看到，从南京电信 -> 上海电信，CN2 GT 是 202.97，而 CN2 GIA 则已经走 59.43 了；
*   CN2 GIA 线路如果本省有 CN2 节点，则直接接入该 CN2 节点。依然从上述两个例子，从江苏南通开始，本省有 CN2 节点（江苏南京），所以 CN2 GIA 线路直接在江苏南京接上了 CN2 节点（59.43），之后就是从上海出口；
*   CN2 GIA 线路如果本省没有 CN2 节点，则就近接入北上广的 202.97 节点，再接入该地的 59.43 节点。如图所示，从安徽芜湖电信先接入上海 202.97，再到 59.43，最后出口；

![](https://www.vpsgo.com/wp-content/uploads/2019/02/wuhu-cn2-gia.jpeg)

*   CN2 GIA 如果在 CN2 节点城市，则直接走 CN2 节点（59.43），而 CN2 GT 则会先走 202.97，只有在国际出口处才会走 59.43。如下图所示，在南京直接接入了 59.43 高速节点。（截止目前，包括但不限于以下城市已经有 CN2 节点：成都，南京，西安，武汉，乌鲁木齐，广州，上海，北京）

![](https://www.vpsgo.com/wp-content/uploads/2019/02/nanjing-cn2-gia.jpeg)

*   综上，区分 CN2 GT 和 CN2 GIA 最简单的方法就是在有 CN2 节点的城市（如南京）跑去程路由，经过 202.97 的就是 CN2 GT，直接 59.43 的就是 CN2 GIA。

**四、CN2 VPS 推荐**
----------------

CN2 GIA 的线路更稳、速度更快，所以 [CN2 GIA 价格](https://www.vpsgo.com/tag/cn2-gia%e4%bb%b7%e6%a0%bc "查看CN2 GIA价格的所有文章")也会相对比较高。VPS GO 已经做了关于 CN2 GIA VPS 的详细推荐，系列文章如下：

*   《[美国 CN2 GIA VPS 服务器商家整理和推荐](https://www.vpsgo.com/usa-cn2-gia-vps.html)》
*   《[香港 CN2 GIA VPS 服务器商家整理和推荐](https://www.vpsgo.com/hong-kong-cn2-gia-vps.html)》

下面推荐几家靠谱的提供 CN2 线路的 VPS 商家。

**1、搬瓦工（BandWagonHost）（推荐）**

搬瓦工同时提供 CN2 GT 线路和 CN2 GIA 线路，机房在美国洛杉矶，带宽是 1Gbps，KVM 虚拟，同时，搬瓦工提供电子商务优化版的 CN2 GIA（搬瓦工 DC6 CN2 GIA，CN2 GIA ECOMMERCE），最高提供 10Gbps 带宽。

搬瓦工优惠码： [BWH3HYATVBJW](https://bwh81.net/aff.php?aff=55247 "点击复制")

搬瓦工 DC6 CN2 GIA（CN2 GIA ECOMMERCE），走的 Zenlayer（C3 机房）的 CN2 GIA + Hivelocity，商务优化，最高可提供 10Gbps 带宽，方案汇总如下：

搬瓦工 CN2 GT 线路电信走 CN2 GT，移动部分地区走 CN2 GT，部分走自己的线路，联通则是直连线路，方案汇总如下：

搬瓦工 CN2 GIA 线路是电信 / 移动 / 联通三网都走 CN2 GIA，方案汇总如下（目前便宜方案没有货）：

更多搬瓦工教程整理：《[搬瓦工 VPS 专题：搬瓦工优惠码和搬瓦工新手教程整理](https://www.vpsgo.com/bandwagonhost.html)》

**2、HostDare CN2 GIA**

HostDare 的 KVM 方案电信 CN2 GIA，移动联通直连，同时 HostDare 提供大硬盘服务器，最高 450G 硬盘容量，并且 4G 内存以上的方案可以提供 Windows 服务器，方案汇总如下（优惠码：[HostDare 优惠码：终身 75 折优惠 / 电信 CN2 GIA / 移动联通直连](https://www.vpsgo.com/hostdare-75-promotion-code.html))

**3、GigsGigsCloud CN2 GIA**

GigsGigsCloud 推出的美西 CN2 GIA 线路（洛杉矶机房），也是 1Gbps 的带宽，KVM 虚拟，并且 1G 内存以上方案提供美国原生 IP，电信 / 移动 / 联通三网直连，方案汇总如下（选择 US SimpleCloud V ）：

**4、DMIT CN2 GIA**

DMIT 收购了 HKSS 的[洛杉矶 CN2 GIA](https://www.vpsgo.com/tag/%e6%b4%9b%e6%9d%89%e7%9f%b6cn2-gia "查看洛杉矶CN2 GIA的所有文章")，现在无论是硬件实力还是客户群体上都有了质的飞跃，并且 DMIT 美西 CN2 GIA 的优势是提供美国原生 IP，可以解锁 Netflix 等流媒体。

**5、iON Cloud CN2 GT**

iON 服务器的速度不错，隶属于老牌商家 Krypt，也是很靠谱的一个商家，提供洛杉矶 CN2 GT 线路，价格还比较适中，稳定性不错，方案整理如下：

**6、CN2 GIA 推荐整理**

VPS GO 建议大家选择搬瓦工 CN2 GIA-E，稳定性和商家实力都没话说，老王有 4 台他家的 CN2 GIA 方案，非常不错。演示网站：

1.  搬瓦工 DC6 CN2 GIA：[https://dc6.bwg.wiki](https://dc6.bwg.wiki/)
2.  搬瓦工 DC9 CN2 GIA：[https://dc9.bwg.wiki](https://dc9.bwg.wiki/)   为例，省级出口以上都是 59.43 高速节点，因此是 CN2 GIA 类型：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-traceroute.png)

**回程路线判断**则需要自己的 VPS 上借助 mtr 工具，执行命令`mtr -rw ip`查看回程路由，依然以搬瓦工的 CN2 GIA 线路为例（依然保证省级出口以上都是 59.43 高速节点）：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-gia-mtr.png)

作为参考，再放一张 CN2 GT 线路的去程路由，可以看到 202.97 普通节点的数量明显增多，从南京电信 -> 上海电信依然是 202.97 节点：

![](https://www.vpsgo.com/wp-content/uploads/2019/02/cn2-traceroute.png)

同理，如果是 163 骨干网，那么全程都是 202.97 普通节点。

163 骨干网和 CN2 线路的区别很明显，但是 CN2 GT 线路和 CN2 GIA 线路都走了 59.43 和 202.97 节点，那么应该如何[区分 CN2 GT 和 CN2 GIA](https://www.vpsgo.com/tag/%e5%8c%ba%e5%88%86cn2-gt%e5%92%8ccn2-gia "查看区分CN2 GT和CN2 GIA的所有文章") 呢？

*   CN2 GT 和 CN2 GIA 都保证国家与国家之间的传输在 CN2 骨干网（59.43 节点）上进行，即国际出口走 59.43；
*   CN2 GT 的省级出口为 202.97 节点，只有在国际出口时才会走 59.43，对比上述两张图可以看到，从南京电信 -> 上海电信，CN2 GT 是 202.97，而 CN2 GIA 则已经走 59.43 了；
*   CN2 GIA 线路如果本省有 CN2 节点，则直接接入该 CN2 节点。依然从上述两个例子，从江苏南通开始，本省有 CN2 节点（江苏南京），所以 CN2 GIA 线路直接在江苏南京接上了 CN2 节点（59.43），之后就是从上海出口；
*   CN2 GIA 线路如果本省没有 CN2 节点，则就近接入北上广的 202.97 节点，再接入该地的 59.43 节点。如图所示，从安徽芜湖电信先接入上海 202.97，再到 59.43，最后出口；

![](https://www.vpsgo.com/wp-content/uploads/2019/02/wuhu-cn2-gia.jpeg)

*   CN2 GIA 如果在 CN2 节点城市，则直接走 CN2 节点（59.43），而 CN2 GT 则会先走 202.97，只有在国际出口处才会走 59.43。如下图所示，在南京直接接入了 59.43 高速节点。（截止目前，包括但不限于以下城市已经有 CN2 节点：成都，南京，西安，武汉，乌鲁木齐，广州，上海，北京）

![](https://www.vpsgo.com/wp-content/uploads/2019/02/nanjing-cn2-gia.jpeg)

*   综上，区分 CN2 GT 和 CN2 GIA 最简单的方法就是在有 CN2 节点的城市（如南京）跑去程路由，经过 202.97 的就是 CN2 GT，直接 59.43 的就是 CN2 GIA。

**四、CN2 VPS 推荐**
----------------

CN2 GIA 的线路更稳、速度更快，所以 [CN2 GIA 价格](https://www.vpsgo.com/tag/cn2-gia%e4%bb%b7%e6%a0%bc "查看CN2 GIA价格的所有文章")也会相对比较高。VPS GO 已经做了关于 CN2 GIA VPS 的详细推荐，系列文章如下：

*   《[美国 CN2 GIA VPS 服务器商家整理和推荐](https://www.vpsgo.com/usa-cn2-gia-vps.html)》
*   《[香港 CN2 GIA VPS 服务器商家整理和推荐](https://www.vpsgo.com/hong-kong-cn2-gia-vps.html)》

下面推荐几家靠谱的提供 CN2 线路的 VPS 商家。

**1、搬瓦工（BandWagonHost）（推荐）**

搬瓦工同时提供 CN2 GT 线路和 CN2 GIA 线路，机房在美国洛杉矶，带宽是 1Gbps，KVM 虚拟，同时，搬瓦工提供电子商务优化版的 CN2 GIA（搬瓦工 DC6 CN2 GIA，CN2 GIA ECOMMERCE），最高提供 10Gbps 带宽。

搬瓦工优惠码： [BWH3HYATVBJW](https://bwh81.net/aff.php?aff=55247 "点击复制")

搬瓦工 DC6 CN2 GIA（CN2 GIA ECOMMERCE），走的 Zenlayer（C3 机房）的 CN2 GIA + Hivelocity，商务优化，最高可提供 10Gbps 带宽，方案汇总如下：

搬瓦工 CN2 GT 线路电信走 CN2 GT，移动部分地区走 CN2 GT，部分走自己的线路，联通则是直连线路，方案汇总如下：

搬瓦工 CN2 GIA 线路是电信 / 移动 / 联通三网都走 CN2 GIA，方案汇总如下（目前便宜方案没有货）：

更多搬瓦工教程整理：《[搬瓦工 VPS 专题：搬瓦工优惠码和搬瓦工新手教程整理](https://www.vpsgo.com/bandwagonhost.html)》

**2、HostDare CN2 GIA**

HostDare 的 KVM 方案电信 CN2 GIA，移动联通直连，同时 HostDare 提供大硬盘服务器，最高 450G 硬盘容量，并且 4G 内存以上的方案可以提供 Windows 服务器，方案汇总如下（优惠码：[HostDare 优惠码：终身 75 折优惠 / 电信 CN2 GIA / 移动联通直连](https://www.vpsgo.com/hostdare-75-promotion-code.html))

**3、GigsGigsCloud CN2 GIA**

GigsGigsCloud 推出的美西 CN2 GIA 线路（洛杉矶机房），也是 1Gbps 的带宽，KVM 虚拟，并且 1G 内存以上方案提供美国原生 IP，电信 / 移动 / 联通三网直连，方案汇总如下（选择 US SimpleCloud V ）：

**4、DMIT CN2 GIA**

DMIT 收购了 HKSS 的[洛杉矶 CN2 GIA](https://www.vpsgo.com/tag/%e6%b4%9b%e6%9d%89%e7%9f%b6cn2-gia "查看洛杉矶CN2 GIA的所有文章")，现在无论是硬件实力还是客户群体上都有了质的飞跃，并且 DMIT 美西 CN2 GIA 的优势是提供美国原生 IP，可以解锁 Netflix 等流媒体。

**5、iON Cloud CN2 GT**

iON 服务器的速度不错，隶属于老牌商家 Krypt，也是很靠谱的一个商家，提供洛杉矶 CN2 GT 线路，价格还比较适中，稳定性不错，方案整理如下：

**6、CN2 GIA 推荐整理**

VPS GO 建议大家选择搬瓦工 CN2 GIA-E，稳定性和商家实力都没话说，老王有 4 台他家的 CN2 GIA 方案，非常不错。演示网站：

1.  搬瓦工 DC6 CN2 GIA：[https://dc6.bwg.wiki](https://dc6.bwg.wiki/)
2.  搬瓦工 DC9 CN2 GIA：[https://dc9.bwg.wiki](https://dc9.bwg.wiki/)