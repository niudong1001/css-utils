# css-modules
一个基本的，独立的，可重用的，可扩展的css模块集合。

## 撰写标准
+ 每一个类文件应该独立，可以被单独引入到需要的文件里面（唯一被允许的依赖文件为var.scss）
+ 使用scss撰写类
+ 任何依赖var.scss的类使用-r后缀

## 类文件说明
+ func文件夹:包含任何单属性的基本可用函数
	- func.scss:不依赖var.scss的单值函数 ***可直接被导入***
	- func-r.scss:依赖var.scss的单值函数 ***导入需要var.scss支持***
+ 



