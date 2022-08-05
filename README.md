<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/xminertools/x/main/logo.png" width="350"/>
</h1>

<h4 align="center">基于GoLang的高性能多线程ETH/ETC/BTC矿池转发中继代理工具</h4>

<p align="center">
  <a href="https://t.me/XMinerTools">Telegram 讨论群组</a>
</p>

![Screenshot]

## :sparkles: 特性

* :cloud: 矿池转发：支持ETH/ETC/BTC的中继代理，支持Stratum/NiceHash/Stratum2所有协议，方便统一管理(其他币种即将更新)
* :zap: 超高性能：采用高效率的GoLang语言编写，并对多线程进行优化
* 💻 自定义抽水：支持中继平台自定义抽水比例进行抽水，并支持在不关闭代理池的情况下进行动态修改
* 📚 多种抽水算法：用户可自选各种抽水算法，防止算力出现周期函数或心跳图的情况
* 💾 安全稳定：支持TCP、SSL等方式，并对CC攻击编写一定的策略进行防护
* :gear: 独家前置代理模式：支持中转服务器到矿池端的加密与混淆，可内网部署
* :outbox_tray: 批量转发：一个软件即可开启对多个矿池的转发，无需开启多个进程
* :card_file_box: 热修改：配置均可网页后台上热修改，无需再修改繁琐配置文件再重启
* :art: 精美后台：后台网页功能全面、折线图、统计丰富
* :eye_speech_bubble: 完善社区支持：Telegram 群组内可帮助处理解决遇到的各类问题，欢迎提出反馈建议
* :rocket: 开箱即用：All-In-One 打包，一键搭建运行，一键配置
* :family_woman_girl_boy: 多系统支持：Windows Linux均可支持使用，无需额外环境等
* :gear: 专业团队：拥有丰富区块链开发的工作经验，多名开发人员来自香港科技大学名校
* :link: 快速响应：可选择开启，伪装低延迟(用户内核延迟处显示的延迟为矿机到中转服务器的延迟)、清理无效提交
* 🌈 ... ...


<h2>Linux一键工具箱</h2>
<p>root用户直接执行以下命令, 根据提示选择对应功能即可。</p>

```
bash <(curl -s -L https://raw.githubusercontent.com/xminertools/x/main/linux-install.sh)
```

<h2>免责声明</h2>
<p>法律不支持的地区此程序无法使用，请自觉遵守当地相关政策，使用此软件造成的法律问题，一概与软件作者无关。</p>

# 导航

<ol>
<li>
    <a href="#uplog">更新日志</a>
</li>
<li>
    <a href="#gn">功能</a>
</li>
<li>
    <a href="#install">部署软件</a>
    <ul>
        <li>
            <a href="#linux">Linux</a>
            <ul>
                <li>
                    <a href="#linux">安装</a>
                </li>
                <li>
                    <a href="#linux">更新</a>
                </li>
                <li>
                    <a href="#linux">卸载</a>
                </li>
                <li>
                    <a href="#linux">停止服务</a>
                </li>
                <li>
                    <a href="#linux">启动服务</a>
                </li>
                <li>
                    <a href="#linux">重启服务</a>
                </li>
                <li>
                    <a href="#linux">开机启动</a>
                </li>
                <li>
                    <a href="#linux">设置最大连接数</a>
                </li>
                <li>
                    <a href="#linux">查看程序运行时日志</a>
                </li>
            </ul>
        </li>
        <li>
            <a href="#windows">Windows</a>
        </li>
        <li>
            <a href="#_kenc">本地加密客户端KENC</a>
        </li>
    </ul>
</li>
<li>
    <a href="#about">常见问题</a>
    <ul>
        <li>
            <a href="#q15">内存相关</a>
        </li>
        <li>
            <a href="#q0">进程守护</a>
        </li>
        <li>
            <a href="#q1">默认账号密码</a>
        </li>
        <li>
            <a href="#q1">算力呈现波浪状</a>
        </li>
        <li>
            <a href="#q2">负载均衡</a>
        </li>
        <li>
            <a href="#q3">安装时提示 curl: command not found</a>
        </li>
        <li>
            <a href="#q4">修改端口启动</a>
        </li>
        <li>
            <a href="#q5">修改密码</a>
        </li>
        <li>
            <a href="#q6">启动时提示 dial tcp connection refused</a>
        </li>
        <li>
            <a href="#q7">关闭/删除端口</a>
        </li>
        <li>
            <a href="#q8">安装时提示：安装killall失败！！！！请手动安装psmisc后再执行安装程序。</a>
        </li>
        <li>
            <a href="#q9">WEB访问长时间卡在LOADING界面。</a>
        </li>
        <li>
            <a href="#q11">IP黑名单</a>
        </li>
        <li>
            <a href="#q12">ETH、ETC芯片机</a>
        </li>
        <li>
            <a href="#q18">芯动A11系列相关问题</a>
        </li>
        <li>
            <a href="#q13">本地算力修改</a>
        </li>
        <li>
            <a href="#q14">迁移</a>
        </li>
        <li>
            <a href="#q10">开发费用及算力损失问题</a>
        </li>
        <li>
            <a href="#q16">观察者链接</a>
        </li>
        <li>
            <a href="#q17">算力跑不够的常见原因</a>
        </li>
    </ul>
</li>
<li><a href="#about">免责声明</a></li>
<li><a href="#about">联系我们</a></li>
</ol>

<span id="gn"></span>
### 核心功能

- 全币种无损抽水
- 先进的内存管理机制, 单机最高8000台稳定运行至今
- 精确到单台设备的24小时数据统计分析
- TLS/SSL/KENC加密
- 配套的本地端加密工具
- 预置各币种矿池（随时更新）
- 软防cc
- 多钱包配置
- 替换指定钱包
- 统一钱包
- 矿池模式
- 快捷导入到出所有配置
- 修改矿池内本地算力
- IP黑名单
- 自定义RSA加密密钥
- 自定义证书
- 自定义配置
- 掉线提醒
- 矿池官网一样的观察者地址
- 超低的手续费

### 已支持抽水的币种（如需增加新币种, 请在电报内联系管理员, 通常一天之内就可以完成）

- BTC
- ETC
- ETH
- LTC
- ERG
- CFX
- RVN
- SERO
- XMR
- CKB
- BEAM
- ALPH
- KASPA
- ...

<span id="uplog"></span>
# 更新日志

```
V2.7.6更新内容：
此次版本为大版本更新，软件重新制作优化，强烈建议更新。
新增加BTC抽水
更新精准抽水算法，降低抽水损耗，适配跨矿池抽水和动态难度)
针对矿池链接稳定性进行独家优化，降低因服务器网络波动导致的损耗
针对大量矿机的高并发环境进行优化
大幅优化CPU和内存占用情况
优化网络带宽使用
修复前置代理模式的代理池初始化timeout问题
修复数个BUG
```

<!-- GETTING STARTED -->
<p id="install"></p>


<p id="linux"></p>

# Linux

```
root用户直接执行以下命令, 根据提示选择对应功能即可。
bash <(curl -s -L https://raw.githubusercontent.com/x/xminertools/main/linux-install.sh)
```
### 安装完成之后, 请立即修改登录账号、密码以及启动端口，防止被爆破。



支持的Linux

* Ubuntu 64 18.04+
* Centos 64 7+

<p id="windows"></p>

# Windows
下载完后直接启动即可，程序自带进程守护

<a href="https://github.com/x/xminertools/tree/main/Windows-64">下载地址</a>
<span id="_kenc"></span>
# KENC
<p>
请前往<a href="https://github.com/x/xminertools/tree/main/KENC">https://github.com/x/xminertools/tree/main/KENC</a>自行下载
</p>
<p><a href="#kenc">KENC帮助文档</a></p>


<p id="question"></p>
<p id="about"></p>

# 常见问题

<span id="q0"></span>
## 进程守护
<p>程序自带了进程守护, 不要！不要！不要使用supervisor或相关工具维护进程，否则会导致进程重复开启。</p>

<span id="q1"></span>
## 算力呈现波浪状

<p>如果出现上述中的情况, 说明您开启了多个相同端口的KTMinerproxy, 关闭多余的进程即可。</p>
<p>如果您进行了镜像拷贝，也会出现以上问题，先执行脚本停止程序的运行，然后删除掉/root/ktmproxy/license文件, 再执行启动即可</p>

<span id="q2"></span>
## 负载均衡
<p>...</p>

<span id="q3"></span>
## 安装时提示 curl: command not found
<p>安装时提示 curl: command not found， 说明你的linux没有安装curl</p>
<p>先执行    apt-get update</p>
<p>然后执行  apt install curl</p>
<p>等待命令执行完毕，即可执行安装脚本</p>

<span id="q4"></span>
## 修改端口启动
<p>执行安装脚本，选择修改端口启动，输入要修改的端口号即可。</p>

<span id="q5"></span>
## 修改密码
<p>安装完后请尽快前往设置页修改密码。</p>

<span id="q6"></span>
## 启动时提示 dial tcp connection refused
<p>请将ktproxy.com添加至防火墙白名单中，这个域名提供了图表服务及认证</p>

<span id="q7"></span>
## 关闭/删除端口

<p>点击指定位置即可删除/关闭端口</p>

<span id="q8"></span>
## 安装时提示：安装killall失败！！！！
<p>检查服务器的镜像源并手动安装psmisc</p>

<span id="q9"></span>
## WEB访问长时间卡在LOADING界面。
<p>安装或更新后，第一次访问web界面加载时间可能会有些长，如果很长时间没有进去，请更换chrome浏览器。</p>

<span id="q1"></span>
## 默认账号密码
<p>默认账号: admin</p>
<p>默认密码: admin123</p>

<span id="q10"></span>
## 开发费用及算力损耗
<p>开发费用恒定至千分之三</p>
<p></p>
<p>多种原因会造成算力损耗，检查以下项，不要什么屎盆子都往开发者头上扣</p>
<p></p>
<p>观察矿池内延迟份额的比例，如果延迟率高于百分1请ping服务器检查延迟</p>
<p></p>
<p>抽水的算力因池而异，如果两个池子难度不同，也会导致算力差异</p>

<span id="q11"></span>
## IP黑名单
<p></p>
<p> 前往设置页面, IP黑名单选项卡可主动加入IP黑名单</p>
<p></p>
<p><img src="./image/jt18.png"></p>
<p></p>

<span id="q12"></span>
## ETH、ETC芯片机
<p></p>
<p> 常见的如奶牛、茉莉、亚米等机型, 需要用ETH端口, 芯动系列或其他的机型请选择ETH(GetWork)端口</p>
<p> 如果设备无法正常接入，不同类型的端口可以交替着试一下。</p>
<p></p>

<span id="q18"></span>
## 芯动A11系列相关问题
<p></p>
<p> A11抽水矿池需要和目标矿池相同。</p>
<p> 如果同池还存在高无效的情况, 请降级或升级固件至a11_20211026_060307版本, mx需要降级或升级至 a11mx_20211220_124402版本。</p>
<p></p>

<span id="q13"></span>
## 本地算力修改
<p></p>
<p> 添加或编辑端口时, 在【高级】选项卡下可进行ETH、ETC的本地算力修改</p>
<p></p>

<span id="q14"></span>
## 服务迁移
<p></p>
<p> 无论使用任何方式迁移程序, 迁移之后请将新的目录下license文件删除, 然后重启程序</p>
<p></p>

<span id="q15"></span>
## 内存相关
<p></p>
<p> 目前单台设备内存占用峰值控制在1.5M, 处于长期观察调整阶段, 之后会根据实际情况调低占用, 请根据接入设备数</p>量来决定硬件配置
<p></p>

<span id="q16"></span>
## 观察者链接
<p></p>
<p> 打开 端口设置-高级设置 ， 找到观察者链接，打开并保存，端口详情页内左下角找即可找到观察者链接。</p>

<span id="q17"></span>
## 算力跑不够的常见原因
<p>如果测试下来24小时均值和设置的差距过大的话, 比如设置抽百分之1, 均值却少了很多, 有很多原因会导致这种情况发生，需要自己一步步排查。</p>
<p>通常检查本地是否中招，或是设备出现问题，例如中转里某些设备无效率很高，这种情况通常是卡出问题了, 找到到这种情况通常比较容易排查，在KT中找到高无效的设备，点开后看下日志里是否有很多POW相关的关键字，如果有的话那么就说明这台设备的硬件出问题了，导致无效引发算力偏低。</p>
<p>更常见的一种原因是本地中招，这个非常容易遇到但是不好排查，可以在KT里建立一个纯转发的端口，用纯转发的端口测试设备24小时均值，如果纯转发的端口24小时跑不够，那么大概率是本地中招，本地重新安装干净的系统解决。</p>

# 免责声明
<p id="flsm">
开发者仅在技术及爱好的驱使下维护此软件，本软件仅验证技术过程。

用前请遵循当地法律，不允许的区域内禁止使用。

使用此软件造成的法律问题, 一概与软件作者无关。
</p>


# 联系我们

<p>Telegram: <a href="https://t.me/xminertools">https://t.me/xminertools</a></p>
<p>QQ群聊: <a href="https://jq.qq.com/?_wv=1027&k=DAlI9VbO">https://jq.qq.com/?_wv=1027&k=DAlI9VbO</a></p>

<p align="right">(<a href="#top">back to top</a>)</p>


## :scroll: 开发抽水
* 0.3%
