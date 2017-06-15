# echarts3.0与echarts2.0的一些区别

### 写在前面:
	昨天在做四大平台的大屏的时候,查看了echarts的官网,突然发现echarts官网界面炫酷高大上了许多,焕然一新的面貌忍不住去多看了几眼.发现从底层的技术架构到上层的外观展现,都相比于2.0进行了较大的升级.根据官方以及其他博客上面给出的升级后一些区别,这里简单罗列下,后续在慢慢具体补充.
[官方给出的echarts2 升级到 echarts3 说明](https://github.com/ecomfe/echarts/issues/3322)
[ECharts 3 带来了什么](http://efe.baidu.com/blog/whats-new-in-ec3/)

#### 1、引入方式简化
[echarts 2.0](http://echarts.baidu.com/echarts2/doc/start.html)
[echarts 3.0](http://echarts.baidu.com/tutorial.html#5%20%E5%88%86%E9%92%9F%E4%B8%8A%E6%89%8B%20ECharts)
#### 2、参考文档API的展示
    echarts 2.x参考文档还是比较详细的，里面会介绍基本图表的一些知识，让你明白什么是坐标系，什么是序列数据，什么是配置项，每种图表是哪种样子？
    没有编程基础的童鞋也没关系，查找一下相似实例，基本上在例子的基础上，修改一下属性，看一下实时效果是没有问题的。
    echart3.x的参考文档显得就比较高大上了，事件API文档打开，一共4项。
    - 全局ECharts对象：[echarts](http://echarts.baidu.com/api.html#echarts)
    - 通过 echarts.init 创建的实例：[echartsInstance](http://echarts.baidu.com/api.html#echartsInstance)
    - ECharts 中支持的图表行为，通过 dispatchAction 触发：[action](http://echarts.baidu.com/api.html#action)
    - ECharts 中的事件列表：[events](http://echarts.baidu.com/api.html#events)
    如果想修改一下特性，又不知道具体的属性是什么，这时候第一靠猜，第二是慢慢找了。不过基本上你对最外层的属性熟悉了，再去找也就自然而然了。

**举个例子**
*问：如何想修改柱状图的颜色？*
答：第一肯定想到[series](http://echarts.baidu.com/option.html#series)序列，bar图表里面的属性基本没有什么特殊性，与line，pie基本都是一样的，一共也只有22个属性，大致浏览一下也只需要1分钟时间，会定位到[itemStyle](http://echarts.baidu.com/option.html#series-bar.itemStyle)类似这样的样式属性上，接下来只需要细看文档就好了。
#### 3、待整理
