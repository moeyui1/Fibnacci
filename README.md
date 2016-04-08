# 斐波那契数列的nasm汇编实现

----------

用nasm写了一个nasm的斐波那契数列计算，可以根据输入的数字来让程序输出对应的斐波那契数列值。程序还会调用linux的彩色输出来以不同的颜色显示不同的结果。

只在linux 64位上成功运行，fb.asm就是源码（只能f(90)左右），bigdata.asm是改进后的版本（主要就是突破第一次溢出），其他都是测试用。

## 算法实现

主要难点在于斐波那契数到一定数值之后突破64位上限溢出，本程序的处理是采用**本数+上限数*n **的方式进行数据存储，这样就可以大大增加了可存储的上限。

但是第一次溢出后n也开始呈现斐波那契数增长，所以很快（大概f(180)左右）就会达到n的上限值，此时再对n进行**本数+上限数*n1 **的方式进行数据存储，理论上可以达到f(270),然后再对ni进行。。。。。

由于汇编实在太烦，我只写到f(180)左右，也就是达到第二次溢出。有空~~应该也不会有空~~再完善吧。

## 目前进度

闲置中。。。。


