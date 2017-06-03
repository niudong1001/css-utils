## Grid
+ 网格布局类

## 规范
+ 所有类用g-为前缀

## 注意
+ 布局主要使用float
+ 建议所有g-col中包含子对象div进行操作

## 主要类介绍
+ g-row : 所有g-col-*的父类
+ g-col : 所有列必须包含
+ g-col-* : width=*/12的列
+ g-col-$-* : width=*/12的列($:sm,md,lg)
+ g-offset-* : margin-left=*/12的列
+ g-offset-$-* : margin-left=*/12的列($:sm,md,lg)

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
