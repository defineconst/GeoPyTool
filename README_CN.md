Title: GeoPython，用于地质学的日常工作的 Python 工具集
Date: 2016-12-18 16:20
Category: Python

#[GeoPython，用于地质学的日常工作的 Python 工具集](https://github.com/cycleuser/GeoPython)

#####author: cycleuser
#####email: cycleuser@cycleuser.org
#####Copyright 2017 cycleuser


|MileStone|Date|Function|
|--|--|--|
|Beginning Date|2016-07-07 6:20|TAS|
|Adding QAPF|2016-07-09 08:32|QAPF|
|Adding Wulff|2016-12-18 08:32|Wulf|
|Reconsitution|2017-03-15 15:30|Wulf|

##j简介


GeoPython 是一个将 Python 用于地质学的日常工作的计划。这是一套自由软件：你可以重新分发或者做出修改，但必须基于由自由软件基金会发布的GNU通用公共许可证第三版的许可,或其后的版本。

##依赖关系

GeoPython 是在 Python 3.5 下写的，基于 numpy， matplotlib， xlrd 以及 pandas。所以这几个包你都得安装。

用PIP就可以安装了：

```Python
pip install numpy
pip install matplotlib
pip install pandas
pip install xlrd
```

##在Windows系统中使用

我已经将程序功能打包成了一个个单独的 zip 包，内置了 exe 文件和 使用的 数据文档样本。可以在[这里下载](https://github.com/cycleuser/GeoPython/tree/master/Windows)，解压缩之后，把你的数据按照示范放到模板文件中，然后双击对应名字的exe程序就行了。


##在 Python 中使用

推荐在 Python 中使用，这样可以使用到最新的开发版本，体验到全部最新的功能。安装方法很简单，使用 pip 即可：


```Bash
pip install geopython
```

然后打开你的python，进入到数据目录，目前样本数据文件还要在[这里](https://github.com/cycleuser/GeoPython/blob/master/Python/DataFileSamples.zip)下载。下载好样本文件，把自己的数据填入，然后用下面的命令就可以运行了：

```Bash
ipython
```

```Python
import geopython as gp

gp.Tas("tas.xlsx").read()               # TAS 图解
gp.Ree("ree.xlsx").read()              # REE 稀土元素图解
gp.Trace("trace.xlsx").read()              # 微量元素蛛网图
gp.Trace2("trace.xlsx").read()              # 另一种组合的微量元素蛛网图
gp.Qfl("qfl.xlsx").read()              # QFL 大地构造图解
gp.Qmflt("qmflt.xlsx").read()              # Qmflt 大地构造图解
gp.QapfP("qapf.xlsx").read()              # Qapf 图解，适用于深成岩
gp.QapfV("qapf.xlsx").read()              # Qapf 图解，适用于喷出岩
gp.Polar("strike.xlsx").read()              # 构造产状的吴尔夫网和施密特网投图
```

一定记得，只有先导入了模块，才能使用里面的功能。

导入完毕后，根据我提供的样板文件，把你的数据输入进去。

如果python提醒你找不到excel的xlsx文件，很可能就是你进错目录了，那样你就需要找到你下载并修改的xlsx文件的位置，用cd命令进去，然后再进行上面的操作。

然后你就在程序中如下所示这样读取一下，然后用对应模块的函数帮你搞定一切了。（注意大小写！）

如果你的数据文件没有什么问题，你就能得到图像了，这些图像会存放在excel表格文件所在的同一目录下：

* 一个碉堡的 svg（一种矢量图）文件，直接就能用Adobe Illustrator 或者 Corel Draw来打开编辑。

* 然后就是一个png图像了。


TAS:
![](https://github.com/cycleuser/GeoPython/blob/master/tas.xlsxtas.png?raw=true)

Trace:
![](https://github.com/cycleuser/GeoPython/blob/master/trace.xlsx.png)

Ree:
![](https://github.com/cycleuser/GeoPython/blob/master/ree.xlsx.png?raw=true)

QFL:
![](https://github.com/cycleuser/GeoPython/blob/master/qfl.xlsxqfl.png)

QAPF:
![](https://github.com/cycleuser/GeoPython/blob/master/qapf.xlsxqapfP.png?raw=true)

Wulf:
![](https://github.com/cycleuser/GeoPython/blob/master/strike.xlsxWulff.png)

Schmidt:
![](https://github.com/cycleuser/GeoPython/blob/master/strike.xlsxSchmidt.png)


