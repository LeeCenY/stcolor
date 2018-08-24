stcolor: 在Stata绘图中使用中国和日本传统色<img src="https://github.com/czxa/Web_data_Source/raw/master/e_learning.png" align="right" />
========================================================
[![](https://img.shields.io/badge/My-Stata-brightgreen.svg?style=plastic)](http://www.czxa.top) [![](https://img.shields.io/badge/github-Stata-orange.svg?style=plastic)](http://www.czxa.top) [![](https://img.shields.io/badge/platform-Mac_OS|Windows_OS-orange.svg?style=plastic)](http://www.czxa.top) [![](https://img.shields.io/badge/Fork-0-orange.svg?style=social)](http://www.czxa.top)

这个程序包里面包含了284个Stata颜色文件和两个Stata绘图命令。

这两个命令——`cncm`和`jpncm`可以绘制出一些颜色板，或者称之为颜色地图。同时为了能够直接使用这些颜色，我还编写了284个颜色文件，安装好这些文件就能直接使用所有的颜色了。

## 安装

### 安装方法一：

```py
net install stcolor, from("http://www.czxa.top/stcolor")
```

### 安装方法二：

* 首先你需要安装github命令，这个命令是用来安装github上的命令的：

```py
net install github, from("https://haghish.github.io/github/")
```

* 然后就可以安装这个命令了：

```py
github install czxa/stcolor, replace
```

### 安装方法三：

* 另外你也可以从这里把ado文件和sthlp文件下载下来，然后放在你的Stata系统文件夹里，查看系统文件夹的路径可以运行下面的命令：

```js
sysdir
```

* 放在那个文件夹里都可以，推荐放在plus文件夹里。


## 使用
&nbsp;|cncm|jpncm
:---:|:---:|:---:
作用|绘制中国传统色地图|绘制日本传统色地图
基本语法| cncm | jpncm
&nbsp;|cncm, c(1)|jpncm, c(red)
&nbsp;|cncm, c(2)|jpncm, c(brown)
&nbsp;|cncm, c(3)|jpncm, c(green)
&nbsp;|&nbsp;|jpncm, c(yellow)

### 两个命令的运行结果

中国传统色|日本传统色
:---:|:---:
![](http://www.czxa.top/mr/20180716a5.png)| ![](http://www.czxa.top/mr/20180716a8.png)
![](http://www.czxa.top/mr/20180716a6.png)| ![](http://www.czxa.top/mr/20180716a9.png)
![](http://www.czxa.top/mr/20180716a7.png)| ![](http://www.czxa.top/mr/20180716a10.png)
![](http://www.czxa.top/mr/20180716a5.png)| ![](http://www.czxa.top/mr/20180716a11.png)

### 安装好之后的颜色使用示例
另外的284个颜色文件的作用就是是的上面图片上的颜色可以被直接使用，例如：

```stata
cd "~/Desktop"
cncm //选择一个颜色
sysuse auto, clear
tw sc price headroom, msize(med) mc(章丹) || ///
  lfit price headroom, lw(*1.5) lc(十样锦) ///
  by(for, note("") leg(pos(6) row(1))) sch(plotplain)
```

![](http://www.czxa.top/mr/20180716a12.png)
