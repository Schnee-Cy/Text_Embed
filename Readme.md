# 数字水印（**Digital Watermarking**）



#### 1.项目起源：

​	微信公众号 **[Crossin的编程教室](javascript:void(0);)**  中有这么一片文章[【每周一坑】图像的指纹：数字水印 + 【解答】鸡兔同笼](https://mp.weixin.qq.com/s/sgYKbf1VqjF-UvQiIDLzgQ	) 

​	学习python之余发现有这么一个数字水印的技术，觉得挺好玩的于是便实现出来。



#### 2.项目信息：

​	作者：苏梓煌   中山大学-2016级-计算机科学与技术		邮箱：<suzh9@mail2.sysu.edu.cn>

​	开发语言：Python 3.6.4 	运行平台：Linux/Windows



#### 3.项目思路：

​	文章中的思路已经说明的很是清楚了，主要思路是我们知道图像是由一个一个的像素点构成的，而每个像素点是由rgb三原色组成，也就是说每个点可以表示为（0-255，0-255，0-255）的一个tuple。由于人眼识别的能力有限，修改最后一位是无法用肉眼发现差异的，如果我们能够将这些数据的最后一位提取出来作为信息位存储信息，那么便能够向图片中嵌入信息啦。



#### 4.版本更新：

​	V1.0 目前能够实现命令行操作下向图片中嵌入一段文字（可支持中文）。

​	V1.1 提供web端接口 [Schnee text-embed](https://www.schnee.pro/lab/text_embed/) ，作为个人网站的测试功能。

​	V1.2 web端提供密码加密功能，也可选择不加密。



#### 5.其他：

**相关博客：**

[Schnee 数字水印（文字嵌入）](https://www.schnee.pro/blog/blog/47)

[CSDN 数字水印（文字嵌入）](https://blog.csdn.net/empire_03/article/details/82262680)



**文件说明：**

###### 	1.build 文件夹下是使用cxfreeze打包好的可执行文件（Windows）

###### 	2.**Digital_watermarking**.py 是可执行文件的源代码，增加了用户交互

###### 	3.**Digital_watermarking**_origin.py 是原始代码，仅提供原始思路

​	当然，数字水印是个很大的范畴，有很多实现方式，具有不同的**实现难度、信息容量、抗攻击性、对原图的干扰**等。我们在这里实现的是最简单的一种方法，其他更加高深的方法还是有待探索的。