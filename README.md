# Dell-Precision-5510-OSX
* Dell-Precision-5510 i7-6820HQ HD530 16G-DDR4 4k-Screen Asgard-AN1-NVMe-SSD-1T DELL-DW1560  
* currently on macOS Catalina (Version 10.15)
* This repo is based on
[scottsanett repo](https://github.com/scottsanett/M5510-4K-High-Sierra-Installation) and 
[darkhand repo](https://github.com/darkhandz/XPS-9550-Mojave)

# HDMI
Inorder for hdmi to be able to output, you should add   
```
				<key>Mac-A5C67F76ED83108C</key>
				<string>none</string>
```  
under `ConfigMap->dict` in `/System/Library/Extensions/AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist`  
and rebuild kext cache using 
`sudo kextcache -i /`  
