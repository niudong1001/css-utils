## Func
+ 任何单值属性的基本函数类

## 规范
+ 所有类用f-为前缀
+ 命名为f-意义两部分组成

## 文件说明

### 导入部分
+ func.scss:不依赖var.scss的单值函数 ***可直接被导入***
+ func-r.scss:依赖var.scss的单值函数 ***导入需要var.scss支持***

### 测试部分
+ sets.scss:func集合，包含func,func-r,../var ***仅用于测试***
+ test.html:func测试页面 ***仅用于测试***
+ sets.css:编译sets.scss后文件 ***仅用于测试***