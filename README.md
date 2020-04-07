# BluePill--STLinkV2
Convert your STM32F103C8T6 "BluePill" Board to an ST-LinkV2
## 简体中文
### 将你的STM32F103C8T6核心板制作成一个ST-LinkV2
> 偶然间发现目前市场上主流的STLinkV2(某宝那种，迷你型的)主控都采用的是STM32F103C8T6，手头正好有一块以这个为主控的最小系统板，也就是被外国网友叫做`Blue Pill`的那个。
> 于是查找相关资料，主要就是STLinkV2的原理图。在洞洞板上进行了简单的焊接。

---
主要的步骤就是 
**刷入固件->更新固件->MDK的配置->完成**
---
采用ISP方式刷入固件，采用CH340G串口下载模块进行下载，上位机选用FlyMCU。
连接方法如下：
+ TX->PA10
+ RX->PA9  
**固件采用的是STLinkV2.J16.S4.hex**
有的同学可能会说：
> 你这个固件版本太老了

不用担心，接下来我们需要安装ST出品的`ST-Link Utility`软件来更新固件。
下载链接是：
    https://www.st.com/zh/development-tools/stsw-link004.html
安装后怎么更新固件，在`Baidu`里十分详尽的说明。

---
MDK中选择`STLINK-V2 Debugger`即可
---
提供Hex格式的固件以及改装所需要的原理图(原理图可能会晚几天到，我之前是在纸上起草的原理图)
