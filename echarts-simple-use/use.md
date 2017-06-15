# 使用方式

#### 放置图表的div
```html
<div id="chart"></div>
```
#### 初始化图表
```javascript
//基于准备好的dom，初始化echarts图表
var myChart = echarts.init(document.getElementById('chart'));
```
NOTE:为了减少复杂的配置文件，我们直接引入echarts-all.js文件，可以满足大部分需求。

#### 设置option
```javascript
var  option = {
	title:'',
	tooltip: {
		trigger: 'item',
		formatter: "{a} <br/>{b}: {c} ({d}%)"
	},
	color: ['#2659a0', '#ebaa01', '#dd452c', '#5d814e'],
	legend: {
          show:true,
          orient: 'vertical',
          x: 'left',
          data:['综合执法','综治工作','其他','市场监管']
      },
	series: [
		{
			name:'特殊人群',
			type: 'pie',
		    radius: ['38%', '60%'],
		    itemStyle: {
				normal: {
					label: {
						show: true,
						formatter: "{b}:{d}%"
					},
					labelLine: {
						show: true
					}
				}
			},
			data: [
				{value: 25, name: '综合执法', itemStyle: {normal: {color: '#2659a0', label: {show: true}, labelLine: {show: true}}}},
				{value: 25, name: '综治工作', itemStyle: {normal: {color: '#ebaa01', label: {show: true}, labelLine: {show: true}}}},
				{value: 25, name: '其他', itemStyle: {normal: {color: '#dd452c', label: {show: true}, labelLine: {show: true}}}},
				{value: 25, name: '市场监管', itemStyle: {normal: {color: '#5d814e', label: {show: true}, labelLine: {show: true}}}}
			]
		}
	]
};
```
#### 加载数据
```javascript
// 为echarts对象加载数据 
myChart.setOption(option);
```