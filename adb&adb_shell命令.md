# adb

1. adb devices 	获取设备列表及设备状态

2. adb get-state 获取设备的状态,  设备的状态有3钟，`device`，`offline` ，`unknown`

   设备：设备正常连接

   离线：连接出现异常，设备无响应

   未知：没有连接设备  

   adb get-serialno 获取设置编号

3. adb kill-server，adb start-server，结束adb服务，启动adb服务，通常两个命令一起用

4. adb logcat，打印Android的系统日志

   adb logcat >d:\log.txt 将log日志打印至d盘log.txt中

5. adb install，安装应用，覆盖安装是使用-r选项,当有多个设备连接时，可以用下面的命令来直接选定设备进行安装。

   adb [-d|-e|-s <serial number>] install <path_to_apk>

   d：真机（多个设备中只有一个真机时适用）

   e：模拟器（多个设备中只有一个模拟器时适用）

   s：序列号

6. adb uninstall [-k]   包名 卸载apk

   -k : 代表保留数据缓存目录

7. adb push <本地路径><设备路径>

   把pc上的文件或文件夹复制到设备中。

   adb push /home/test.apk /sdcard/

   adb pull <设备路径><本地路径>

   把设备上的文件或文件夹复制到电脑

   adb pull /sdcard/log/test.xls /home/

   Pull命令后可不输入本地地址，不输入时文件会复制到当前终端所在目录

8. adb tcpip 9999 ; adb connect 192.168.0.1:9999 adb连接远程连接Android设备 

9. adb logcat -s ActivityManager 查看activity启动时间

10. adb bugreport [-path] 获取bug日志

   -path: 代表手机端日志保存路径

11. adb root 以root权限运行

12. adb unroot 用非root权限运行

13. adb usb 用usb重启



# adb shell

1. adb shell pm list package 列出安装在设备上的应用包名

   -s：列出系统应用  adb shell pm list package -s

   -f :列出应用包名及对应的apk名及存放位置  adb shell pm list package -f

2. adb shell pm clear 包名 清除缓存

3. adb shell am start -n com.sankuai.meituan/com.sankuai.meituan.activity.Welcome 启动app

4. adb shell ps 查看当前运行的进程

5. adb shell cat proc/<进程pid>/oom_adj 查看当前进程优先级,4,5结合使用

6. adb shell dumpsys batterystats --enable full-wake-history 允许获取电量数据；adb shell dumpsys batterystats –reset 重置当前电量数据 ；adb bugreport 获取电量数据

