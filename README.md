# css-modules
一个基本的，独立的，可重用的，可扩展的css模块集合。

## 撰写标准
+ 每一个类文件应该独立，负责自己需要引用的类。
+ 任何依赖```var.scss```的类使用-r后缀。

## 类文件说明
+ func文件夹:包含任何单属性的基本可用函数
+ gird文件夹：grid布局
+ button文件夹：按钮
+ base文件夹：基本样式，如font-size等
+ reset文件夹：重置浏览器样式
+ unit文件夹：常用组件
+ mixins文件夹：mixins集合
+ animation文件夹：动画相关
