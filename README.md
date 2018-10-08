# CSS-Utils

一个基本的，独立的，可重用的，可扩展的css模块集合。

## 撰写标准
+ 每一个类文件应该独立，负责自己需要引用的类。
+ 任何依赖`var.scss`的类使用-r后缀。

## 目录说明
+ `func`: 包含任何单属性的基本可用函数。
+ `gird`: grid布局。
+ `button`: 按钮样式。
+ `base`: 基本样式设置，如font-size等。
+ `reset`: 重置浏览器样式。
+ `unit`: 常用单元组件。
+ `mixins`: mixins集合。
+ `animation`: 动画相关。
