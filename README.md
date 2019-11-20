# Dell-Precision-5510-OSX
* Dell-Precision-5510 i7-6820HQ HD530 16G-DDR4 4k-Screen Asgard-AN1-NVMe-SSD-1T DELL-DW1560  
* 版本 Catalina (Version 10.15)
* 感谢 @黑果小兵 and 
[moshuixin123 pcbeta](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1824016) and
[darkhandz repo](https://github.com/darkhandz/XPS-9550-Mojave)

### 耳机拔插(Other/ComboJack)

它的作用：检测耳机拔插，修复耳机孔多合一下产生的一些问题，关于它的原理，请看[wmchris的教程](https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/10.12/Post-Install/AD-Kexts/Audio/VerbStub_knnspeed/README.md)。

- 执行命令：`cd 把ComboJack文件夹拖过来`
- 执行命令：`chmod +x install.sh`
- 执行命令：`./install.sh`

看见`Enjoy!`的话，ComboJack就安装完成了，重启一下系统。

### HDMI
开启HDMI和usbtypec等外接显示器

在S/L/E, AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist里ConfigMap下添加

```
				<key>Mac-A5C67F76ED83108C</key>
				<string>none</string>
```  
然后重建缓存
`sudo kextcache -i /`
