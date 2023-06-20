# tengine-offline-installer

顾名思义，就是`tengine`服务器的离线安装包，在服务器无法连接网络时可以使用这个离线包安装tengine

关于tengine的更多内容，可以访问官方[github](https://github.com/alibaba/tengine)或者[官网](https://tengine.taobao.org)

## 安装环境要求

目前只支持`CentOS-7.6-x86_64`以上版本, 建议使用无更改的干净系统; 如果你熟悉shell，可以自定义安装过程

其它操作系统的安装文件正在制作中

## 如何使用

访问[release](https://github.com/zhaojul/tengine-offline-installer/releases),下载最新的安装包文件，上传到服务器后解压进行安装

```
tar -zxf tengine-offline-installer-v2.4.1.tgz
cd tengine-offline-installer-v2.4.1
./install.sh
```

## 其他问题

* 如果可以访问公网或者内网yum源，可以将`install.sh`脚本中安装rpm包的步骤注释掉，`cat rpm-packages/README.md`查看需要安装哪些包，可以手动进行安装
* 这个安装包中默认加入的模块比较多，正常使用是用不到这么多的，可以修改`install.sh`和`config/modules.conf`去掉一部分
* 有其它问题，可以提交[Issues](https://github.com/zhaojul/tengine-offline-installer/issues)

