# css-modules
一个基本的，独立的，可重用的，可扩展的css模块集合。

## 撰写标准
+ 每一个类文件应该独立，可以被单独引入到需要的文件里面（唯一被允许的依赖文件为```var.scss```）。
+ 使用scss撰写类。
+ 任何依赖```var.scss```的类使用-r后缀。
+ 任何文件夹中都包括```sets.scss```,```sets.css```,```test.html```,这三个文件仅用于测试。
+ 类命名按照基本名称--样式方式命名。
+ 所有@mixin以```m-```开头。

## 类文件说明
+ func文件夹:包含任何单属性的基本可用函数
	- ```func.scss```
	- ```func-r.scss```
+ gird文件夹：grid布局
	- ```grid-r.scss```
+ button文件夹：按钮
	- ```button.scss```
+ color文件夹：颜色控制
	- ```color-r.scss```
+ font文件夹：font-*属性控制
	- ```font-r.scss```
+ reset文件夹：重置
	- ```reset.scss```
	- ```reset--normalize.scss```
+ unit文件夹：常用组件
	- ```unit.scss```
	- ```unit-r.scss```



