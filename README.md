## 简介
pmonitor 是一个简单的确保程序运行的shell脚本，pmonitor 通过nohup命令使程序运行在后台，并且监控进程是否存在，如果程序发生未知异常退出了，pmonitor会自动重新
启动程序。

## 安装
pmonitor 需要超级用户权限，并且默认的工作路径是当前用户的主目录。为了方便使用，推荐把pmonitor 拷贝到系统环境路径中去。或者使用命令：
```
./pmonitor install
```
该命令会将pmonitor 拷贝到/usr/local/bin/目录下。

## 用法
* 比如需要启动爬虫任务spider.py，只需要命令：
```
pmonitor python spider.py
```
它会启动pmonitor 监控脚本，并执行`nohup python spider.py &` 启动爬虫脚本。

* 通过`pmonitor monitor`命令可以单独启动监控脚本（如果你重启计算机的话，这样可以重启所有之前的pmonitor监控的程序。

* 查看使用方法：
```
pmonitor -h
```



