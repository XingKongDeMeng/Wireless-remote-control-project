# Wireless_remote_control_project

- 使用了两个stm32f103c8t6进行无线通信
- 按下sg2的key2，它的D5灯亮，同时最小系统板的灯(PC13)亮；再按一下就熄灭；
- sg2连接有蓝牙模块，通过手机连接蓝牙发送字符a即可打开D3灯，同时最小系统板灯的状态也会改变。

```shell
sg2接线图
蓝牙———串口2
AS32-TTL-100接串口1

最小系统板接线图
AS32-TTL-100接串口1

注意：AS32-TTL-100在使用时需要先配对，在配对完成后MD0，MD1需要接GND
最小系统板通过串口烧录：
TX——-PA10
RX---PA9
同时BOOT0接1，BOOT1接0，使用FLYMCU烧录选择DTR的高电平复位，RTS高电平进BootLoader
，在烧录完成后，需要将BOOT0接0，BOOT1接0
```

