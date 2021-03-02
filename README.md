这是我一个视频的配套代码。
视频是：利用近邻法的弱点实现图片缩小后变成另一张图
https://www.bilibili.com/video/BV1Lf4y1r7dZ

配套代码中，仅generate.py是核心文件，其余的图片神马的，都是赠品。
这个核心文件利用了近邻法缩放的弱点，可以将图a的像素按顺序嵌入到图b中，然后生成图c。图c看起来和图b是基本一样的。不过，在PS软件或者python的PIL模块中使用近邻法把图c缩小到图a的尺寸时，图a就显示出来了。算是一种形式的“幻影坦克”吧。

使用方法：
假设generate.py、图a、图b都在同一目录下，且图a、图b均为png格式。
python generate.py 图a 图b 图c
回车后生成图c。

**注：win10使用时下载PIL库注意点：**  
python的PIL库只支持python2，所以python3的在控制台输入：pip install pillow,安装成功后找到这个文件夹和PIL文件夹，复制到项目里（目前没找到更好的处理办法）
