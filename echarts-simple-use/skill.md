# 小技巧

#### 当数据为零时隐藏指示线
方法一：遍历循环填充data，当数据项value值为零时continue跳过此次循环
方法二：
```javascript
var opt = option.series[0];
lineHide(opt);
//数据为零时隐藏线段
function lineHide(opt) {
  var itemValArr = [];
  $.each(opt.data, function (i, item) {
  itemValArr.push(item.value);
  if (item.value == 0) {
  item.itemStyle.normal.labelLine.show = false;
  item.itemStyle.normal.label.show = false;
  }
});
```
