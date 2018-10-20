# CSS-Utils

一个基本的，独立的，可重用，可扩展的css模块集合。

## 目录说明

- **mixins**: 包含一些有用的mixins，使用方法为：`@include m-fz($base-size,$base-h-sizes)`，包含的mixins有：

```scss
// 用以设置`link`链接样式
@mixin m-link($link-color,$link-hover-color:darken($link-color,5%)){...}
// 设置该类下所有子元素的`font-family`属性置为`$ff`值
@mixin m-ff($ff){...}
// 设置该类下所有子元素的`font-size`属性，基本的font-size为`$fz`，标题的`font-size`为`$hfz`
@mixin m-fz($fz,$hfz){...}  
```

- **base**: 包含一些跟文字，颜色，链接等相关的基本样式类，样式变量参考根目录下文件`var.scss`，包含内容为：

```scss
// font-family样式设置
.ff--apple {@include m-ff($ff-apple);}
.ff--helvetica {@include m-ff($ff-helvetica);}
.ff--noto {@include m-ff($ff-noto);}
.ff--yahei {@include m-ff($ff-microYH);}
// font-size样式设置
.fz--primary {@include m-fz($base-size,$base-h-sizes);}
// color设置
.c--primary {@include m-c($base-text-color, $base-text-color);}
// link链接设置
.link--primary {@include m-link($base-primary-color);}
```

- **func**: 快速调用对应属性与所搭配的常用属性值，例如部分类如下所示：

```scss
// position位置控制
.f-pr{position: relative;}
.f-pa{position: absolute;}
.f-pf{position: fixed;}
// float&&clear浮动与清除浮动控制
.f-fl{float: left;}
.f-fr{float: right;}
.f-cf:before, .f-cf:after {content: "";display: table;}
.f-cf:after {clear: both;}
.f-cf {zoom: 1;}
```

- **grid**: 用于自适应布局的网格类，其使用例子如：

```html
<div class="g-row">
  <div class="g-col g-col-6 bg-blue">g-col-6</div>
  <div class="g-col g-col-6 bg-red">g-col-6</div>
</div>
<div class="g-row">
  <div class="g-col g-col-6 g-offset-6 bg-blue">g-col-6,g-offset-6</div>
</div>
<div class="g-row">
  <div class="g-col g-col-12 g-col-sm-6 g-col-md-3 g-col-lg-1 g-offset-md-9 bg-red ">
    g-col-12,g-col-sm-6,g-col-md-3,g-col-lg-1,g-offset-md-9
  </div>
</div>
```

- **button**: 存储一些常用的按钮样式类别，样例如下：

```html
<button class="btn-skeleton btn-skeleton--primary">skeleton</button>
```

- **reset**: 包含一些常用的重置浏览器默认样式的类，文件介绍如下：

  - reset: 包含一些常用重置类。
  - normalize: 外部通用重置类，具体可见官网。

## 撰写标准

- 每一个类文件应该引用独立，负责自己需要引用的类。
- 任何依赖`var.scss`的类使用-r后缀。
- `_export.scss`用于可在外部引用的基本类。
- `form`与`animation`未作说明，需要补充。
