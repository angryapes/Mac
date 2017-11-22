# Mac

###Xcode
##### Xcode手动清理
打开Finder使用快捷键command+shift+g输入路径即可进入该文件夹

1. 移除DerivedData,建议定期清理，会重新生成

此文件夹内是模拟器运行每个APP生成的缓存文件，删除之后只是再重新运行APP时会重新编译耗时较长，并再次生成缓存文件。
~/Library/Developer/Xcode/DerivedData

2. 移除Archives，可以清理

此文件夹中的内容是用Xcode打包时生成，可以根据是否有用选择性删除，删除之后Xcode->Organizer下的那些打包文件就全被清空了
~/Library/Developer/Xcode/Archives

3. 移除iOS DeviceSupport，建议清理，连接设备会重新生成

此文件夹中保存着对你设备的版本支持，每个版本文件夹都是几个G的大小，只需保留自己设备当前版本的文件夹即可，即使全部删除，再重新连接设备时Xcode会出现Processing symbol files并重新生成相应版本的文件
~/Library/Developer/Xcode/iOS DeviceSupport

4. 移除模拟器文件，可以清理，运行模拟器会重新生成

此文件夹目录下的文件夹全都是以模拟器的UDID命名的，可以查看.default_created.plist文件根据文件夹命名和plist文件中的内容判断各个文件夹是某版本下某设备类型的模拟器，.default_created.plist文件为隐藏文件，需要开启显示隐藏才能查看
~/Library/Developer/CoreSimulator/Devices


