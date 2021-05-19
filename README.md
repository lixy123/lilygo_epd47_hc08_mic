# lilygo_epd47_hc08_mic
epd47 墨水屏远程麦克风 （远程wifi拾音）

一.功能
利用本程序，可以使epd47墨水屏成为远程麦克风, 利用wifi联网进行麦克风拾音监听

二.硬件
1.LILYGO® T5-4.7 inch E-paper ESP32 1块 
2.墨水屏专用的带 HC08，MIC的 插件模块 1块
引脚连接原理:
epd47 MIC
VCC   VCC
12    MIC_DATA
13    MIC_CLOCK
GND   GND

三.代码说明
软件: arduino 1.8.13
库文件:
https://github.com/espressif/arduino-esp32 版本:1.0.6
https://github.com/me-no-dev/ESPAsyncWebServer 
https://github.com/Links2004/arduinoWebSockets
开发板选择：ESP32 DEV Module   
选择好端口执行程序编译,烧录
注：
1.编译代码前，修改代码中的路由器连接参数ssid,password,connectwifi函数的静态IP地址
2.烧录完程序后，用Arduino插件 ESP32 Sketch upload 执行Data目录上传到spiffs (Arduino插件资料:https://github.com/me-no-dev/arduino-esp32fs-plugin)

三.用法
1.墨水屏上电开机
2.用手机或PC打开网页浏览器(浏览器要支持html5例如chrome,需要同一局域网),输入 http://192.168.1.101 会神奇的听到墨水屏传来的 mic采集到的声音.

四.补充
1.代码不支持并发，一次只能一个客户端连接.
2.用电约在50-80ma,不适合仅用电池供电.
