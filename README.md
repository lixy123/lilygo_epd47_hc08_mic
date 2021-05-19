# lilygo_epd47_hc08_mic
epd47 墨水屏远程麦克风 （远程wifi拾音）<br/>

<b>一.功能</b> <br/>
利用本程序，可以使epd47墨水屏成为远程麦克风, 利用wifi联网进行麦克风拾音监听<br/>

<b>二.硬件</b> <br/>
1.LILYGO® T5-4.7 inch E-paper ESP32 1块 <br/>
2.墨水屏专用的带 HC08，MIC的 插件模块 1块<br/>
引脚连接原理:<br/>
epd47 MIC<br/>
VCC   VCC<br/>
12    MIC_DATA<br/>
13    MIC_CLOCK<br/>
GND   GND<br/>

<b>三.代码说明</b> <br/>
软件: arduino 1.8.13<br/>
库文件:<br/>
https://github.com/espressif/arduino-esp32 版本:1.0.6<br/>
https://github.com/me-no-dev/ESPAsyncWebServer <br/>
https://github.com/Links2004/arduinoWebSockets<br/>
开发板选择：ESP32 DEV Module <br/>
选择好端口执行程序编译,烧录<br/>
注：<br/>
1.编译代码前，修改代码中的路由器连接参数ssid,password,connectwifi函数的静态IP地址<br/>
2.烧录完程序后，用Arduino插件 ESP32 Sketch upload 执行Data目录上传到spiffs (Arduino插件资料:https://github.com/me-no-dev/arduino-esp32fs-plugin)<br/>

<b>三.用法</b> <br/>
1.墨水屏上电开机<br/>
2.用手机或PC打开网页浏览器(浏览器要支持html5例如chrome,需要同一局域网),输入 http://192.168.1.101 会神奇的听到墨水屏传来的 mic采集到的声音.<br/>

<b>四.补充</b> <br/>
1.不支持并发，一次只能一个客户端连接.<br/>
2.用电约在50-80ma,不适合仅用电池供电.<br/>
