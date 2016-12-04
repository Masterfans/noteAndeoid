#android adb shell 命令大全
[原文](http://www.cnblogs.com/acpb/archive/2011/05/24/2056026.html)
1. 显示系统中的全部的android平台
	android list targets
2. 显示系统中全部的AVD(模拟器)
	android list avd
3. 创建AVD
	android create avd --name 名称 --target 平台编号
4. 启动模拟器
	emulator -avd 名称 -sdcard ~/名称.img(-skin 1280*800)
5. 删除AVD
	android deleta avd --name
6. 创建SDCard
	mksdcard 1024M ~/名称.img
7. AVD 所在位置
	Linux(~/android/avd) Windows(C:\Documents and Settings\Administrator\.android\avd)
8. 启动DDMS
	ddms
9. 显示当前运行的全部模拟器
	adb devices
10. 对某一模拟器执行命令
	adb -s 模拟器编号 命令
11. 安装应用程序
	adb install -r 应用程序.apk
12. 获取模拟器中的文件
	adb pull <remote> <local>
13. 向模拟器中写文件
	adb push <local> <remotes>
14. 进入模拟器的shell模式
	adb shell
15. 启动SDK,文档,实例下载管理器
	android
16. 卸载apk包
	adb shell 
	cd data/app
	rm apk包
	exit
	adb uninstall apk 包的主包名
	adb install -r apk包
17. 查看adb命令帮助信息
	adb help
18. 在命令行中查看LOG
	adb logcat -s 标签名
19. adb shell 后面跟的命令主要来自:
	源码\system\core\toolbox目录和源码\framework\base\cmds目录
20. 删除系统应用
	adb remount (重新挂载分区,使系统分区可写)
	adb shell
	cd system/app
	rm *.apk
21. 获取管理员权限
	adb root
22. 启动activity
	adb shell am start -n 包名/包名+类名(-n 类名,-a action -d date,-m MIME-TYPE,-c category,-e扩展数据)
23. 发布端口
	设置任意的端口号,做为主机向模拟器或设备的请求端口
	adb forward tcp:5555 tcp:8000
24. 复制文件
	在两个设备之间复制
	adb push <source> <destination> </destination></source>
	例: adb push test.txt /tmp/test.txt
	复制一个目录
	adb pull <source> <destination></destination></source>
	例: adb pull /android/lib/libwebcore.so
25. 搜索模拟器/设备的实例:
	取得当前运行模拟器/设备的实例的列表及每个实例的状态:
	adb devices
26. 查看bug报告
	adb bugreport
27. 记录无线电通讯日志:
	无线电日志很多,可以通过命令,设置记录:
	adb shell 
	logcat -b radio
28. 获取设备ID和序列号:
	adb get-product
	adb get-seriaIno
29. 访问数据库SQLite3:
	adb shell
	sqlite3
	\#cd system/sd/data//进入系统内指定文件夹
	\#ls //列表显示当前的文件夹内容
	\#rm -r xxx//删除xxx文件夹及其里面的所有内容
	\#rm xxx//删除指定的文件
	\#rmdir xxx //删除xxx的文件夹

