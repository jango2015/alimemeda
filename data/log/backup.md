## 0x00 预览：
![image](https://github.com/0x024/alimemeda/blob/master/data/log/exp.png)

## 0x01环境：
[![](https://img.shields.io/badge/Ubuntu-16.04LTS-brightgreen.svg)]()
[![](https://img.shields.io/badge/Python-2.7-brightgreen.svg)]()
[![](https://img.shields.io/badge/OpenCV-3.2.0-brightgreen.svg)]()
[![](https://img.shields.io/badge/ShadowSocks-Linux-brightgreen.svg)]()

```
curl安装：
	sudo apt-get install curl
```

OpenCV 3.2.0——-关于如何安装OpenCV，这里就简单的说一下下，


```
安装依赖包:
      sudo apt-get install build-essential
      sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
      sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev                                   libjasper-dev libdc1394-22-dev
```

```
从百度云上下载OpenCV的源码:So you can also download it in the official
      链接: http://pan.baidu.com/s/1pKEgRyV 密码: r4qv       #这个是最新的OpenCV3.2.0的代码
      链接: http://pan.baidu.com/s/1bo8zIN1 密码: bmek #这个里面有一些模块，比如freetype，face，等需要用到
```
官网的教程里面将两个包分开进行编译，但是里面的许多包我们确实用不到，所以，最好的办法，就是将./opencv_contrib/moudles/freetype和face文件夹直接复制到./opencv/moudles/下

``` 
进行安装
	cd ~/opencv
	mkdir release
	cd release
	cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
	make -j4  #这里的-j4代表怎么说好呢，反正越大，编译的速度越快
	sudo make install
```
这里说一下了。在运行cmake的时候，会下载几个文件，比如
```
ippicv_linux_20151201.tgz，
```
需要挂代理，不挂代理的话，无法通过cmake，关于如何在ubuntu上安装shadowsocks科学上网，我的博客也有写过，
## 0x02 目录树:

![image](https://github.com/0x024/alimemeda/blob/master/data/log/tree.png)

## 0x03 执行:

```
运行前，

	需要将alimemeda.py中的api_key和api_secret换成你的
	需要将./face/FaceAPI.py中的api_key和api_secret换成你的
	(为了便于您测试,我以将我的key放在里面，为了防止多人使用outer_id冲突，希望您后期换成自己的)
	需要将所需要识别的图片放在/img目录下，暂时只可识别一张

```





```java
python alimemeda.py  #运行完毕后，会覆盖原有的图片。
```



