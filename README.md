# EventListeners
一、搭建ftp服务器

搭建ftp服务器

二、思路简介
本文工具主要利用watchdog对文件夹做监听，如发现文件夹中的文件有移动、创建、重命名、修改操作，那么就把对应的修改上传到ftp服务器。如文件夹某文件删除了，那么不对服务端的数据做处理。也就是对ftp服务器的数据做增量更新。

三、模块简介
1. 日志处理模块
日志处理模块主要是设置日志格式，日志输出等

2. ftp模块
主要是基于ftplib库，利用python代码实现文件从ftp服务器上传、下载、删除、移动> 等。

3. watchdog监听模块
利用watchdog对文件夹做监听，如发现文件夹中的文件有移动、创建、重命名、修改操作，那么就把对应的修改上传到ftp服务器。如文件夹某文件删除了，那么不对服务端的数据做处理。

四、使用
1. 下载项目代码
修改synWatch.py中的配置信息，配置信息有ftp服务器的ip地址，ftp用户名、密码。

 ip = 'x.x.x.x'
 username = 'xxxx'
 passwd = 'xxxx'

2. 进行文件监听
# yourpath为你要监听的本地目录
python synWatch.py yourpath



# python文件打包成EXE
例子：
1、使用pycharm安装pyinstaller。

2、找到pyinstaller的安装目录。

C:\Users\lounious\PycharmProjects\untitled\venv\Scripts\pyinstaller-script.py

注意在该目录的母目录下一般有我们的程序文件

C:\Users\lounious\PycharmProjects\untitled

3、将我们要打包的程序copy至pyinstaller的安装目录下：

C:\Users\lounious\PycharmProjects\untitled\venv\Scripts\

4、打开cmd，找到该路径 cd C:\Users\lounious\PycharmProjects\untitled\venv\Scripts\，输入命令pyinstaller -F  *.py

如下图显示，打包成功。

5、此时在Scripts的目录下能够看到已经生成的dist目录和*.spec文件。运行*.exe文件即可。

6、也可以使用命令pyinstaller -F  *.py，该命令会将所有的依赖放到一个文件夹中。相当于-F的解压。
