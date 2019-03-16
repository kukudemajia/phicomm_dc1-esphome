## 斐讯DC1插座通过ESPHOME接入Home Assistant

![image](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/image/%E4%BA%A7%E5%93%81%E5%9B%BE2.jpg?raw=true)

## WHY
众所周知的原因，斐讯服务器已经不能正常访问，插座的APP控制已经无法正常实现，需要有另外的方式实现插座的控制。

已有的方法为内网劫持实现，具体可参考[这里](https://bbs.hassbian.com/thread-5637-1-1.html)。

这次要实现的是通过一个自定义的固件，来完整实现DC1联网控制。

## TUDO LIST
- [x] 分析硬件，获得主要芯片的资料
- [ ] 确定各引脚对应关系
- [ ] 控制实现推演
- [ ] 编写固件
- [ ] 测试功能
- [ ] 发布

## 已知的一些硬件资料
#### WiFi模组
WiFi模组使用的是芯海的[CSM64F02](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/doc/CSM64F02%20WiFi%E6%A8%A1%E7%BB%84%E7%94%A8%E6%88%B7%E6%89%8B%E5%86%8CV1.3.pdf)，经过分析，这款模组和乐鑫的[ESP-WROOM-02](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/doc/esp-wroom-02%E6%8A%80%E6%9C%AF%E8%A7%84%E6%A0%BC%E4%B9%A6.pdf)是一样的。

![image](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/image/WiFi%E6%A8%A1%E7%BB%84.jpg?raw=true)
#### U7
这是一颗扩展类的芯片，具体型号暂时未知。

![image](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/image/U7.jpg?raw=true)
#### U11
这是一颗电量统计用的芯片，具体型号为[CSE7766](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/doc/cse7766%E7%94%A8%E6%88%B7%E6%89%8B%E5%86%8C.pdf)。

![image](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/image/U11%E7%94%B5%E9%87%8F%E7%BB%9F%E8%AE%A1%E8%8A%AF%E7%89%87.jpg?raw=true)
#### 继电器
继电器使用的是[永能家用继电器YX201系列](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/doc/%E6%B0%B8%E8%83%BD%E5%AE%B6%E7%94%A8%E7%BB%A7%E7%94%B5%E5%99%A8YX201.pdf)的产品，控制电压为5V。

![image](https://github.com/Samuel-0-0/dc1-esphome-home-assistant/blob/master/image/%E7%BB%A7%E7%94%B5%E5%99%A8.jpg?raw=true)

## 更新固件方法
等待更新

## 致谢
- killadm：  导出原始固件，提供芯片对比图
- 实验幼儿园小二班扛把子：  测试引脚走向
- Heller： 初期资料整理

## 免责申明
以上纯属个人爱好，因为使用上述方法造成的任何问题，不承担任何责任。

部分图片来源于网络，如果涉及版权，请通知删除。