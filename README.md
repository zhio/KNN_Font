KNN_Font
一个猫眼爬虫字体文件识别的简易程序
之前的猫眼字体文件识别由于字形是固定的，所有采用了对照表的方式
* 下载一个字体，建立字体和文字的关系
* 匹配新的字形和之前有对应关系字形

之前是根据每次刷新网页不同的woff中，但是它所包含的字形相同，来找对应关系

现在同一个数字unicode名不同，字形也不相同了

但是经过观察，同一数字的对象是不相同的，但是区别是微小的，对象中每个坐标的差值较小，这样我们可以通过限定对象的坐标值差值在一定范围内就可以认为是两个相同的数字了

以上思路来自
https://link.zhihu.com/?target=https%3A//github.com/Ingram7/maoyan_font

并在此基础上进行了改进

决定采用机器学习最简单的方法KNN算法

经过简单的训练，只有三组数据（30条），即可将坐标分类

友链：https://blog.csdn.net/qq_29570381/article/details/103035678
