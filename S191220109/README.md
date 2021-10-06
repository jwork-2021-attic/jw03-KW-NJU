# W03-S191220109

1.
代码工作原理：

加密：在SteganographyFactory类中，读取需要加密的java文件和源图片所在位置，传入getSteganography()函数，该函数使用隐写术将文件信息写入图片，得到一张全新的隐写术图，并将新图片命名为【类名.png】。

解密：与W02中不同，W03中的main函数并没有直接使用原有的自动加载，而是改为使用自定义加载器进行加载。通过观察SteganographyClassLoader类的派生关系可知，该类为ClassLoader类的继承类。由于原.java及.class文件已被删除，故无法使用原有的Bootstrap ClassLoader与Extension ClassLoader对BubbleSorter类进行加载，只能使用SteganographyClassLoader类加载。该类中重载的findClass()函数，可以实现读取隐写术图片得到对应的类并将其返回。最后将得到的类传入Geezer类，以完成后续排序工作。

2.
快速排序算法编写进自选图片得到的隐写术图：

![](https://i.loli.net/2021/10/05/B3gofOam9Did8y4.png)

希尔排序算法编写进自选图片得到的隐写术图：

![](https://i.loli.net/2021/10/05/ZwOMentW1uJRgmi.png)


3.
用自己的隐写术图中所包含的排序算法给example的老头赋予排序能力，得到排序结果（动画）:

(1)快速排序

[![asciicast](https://asciinema.org/a/439896.svg)](https://asciinema.org/a/439896)

(2)希尔排序

[![asciicast](https://asciinema.org/a/439897.svg)](https://asciinema.org/a/439897)


4.
测试了
```191220016 陈致远```
生成的图片，算法类型分别为
```快速排序、希尔排序```
均得到了正确结果。

```191220016 陈致远```的快速排序算法隐写术图

![](https://i.loli.net/2021/10/06/QRqpSxAMBDgkbc1.png)

```191220016 陈致远```的希尔排序算法隐写术图

![](https://i.loli.net/2021/10/06/Z8zyKkUjS6oV4Qi.png)