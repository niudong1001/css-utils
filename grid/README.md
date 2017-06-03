## Grid
+ 网格布局类

## 规范
+ 本文件夹下所有类用g-为前缀

## 注意
+ 布局主要使用float
+ 建议所有g-col-*中包含子对象div后进行操作，这样避免padding与background带来的一些问题。

## 主要类介绍
***(i:1->12,$:sm||md||lg)***
+ ```g-row``` : 所有g-col-*的父类
+ ```g-col``` : 所有单列都必须包含
+ ```g-col-i``` : width=i/12的列
+ ```g-col-$-i``` : width=i/12的响应列
+ ```g-offset-i``` : margin-left=i/12的列
+ ```g-offset-$-i``` : margin-left=i/12的响应列

## 使用案例
```html
<div class="g-row">
	<div class="g-col g-col-6 bg-blue">
		1/2(g-col-6)
	</div>
	<div class="g-col g-col-6 bg-red">
		1/2(g-col-6)
	</div>
</div>
<div class="g-row">
	<div class="g-col g-col-6 bg-blue g-offset-6">
		1/2(g-col-6,g-offset-6)
	</div>
</div>
<div class="g-row">
	<div class="g-col g-col-12 g-col-sm-6 g-col-md-3 g-col-lg-1 g-offset-md-9 bg-red ">
		1/2(g-col-12,g-col-sm-6,g-col-md-3,g-col-lg-1,g-offset-md-9)
	</div>
</div>
```
