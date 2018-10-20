# CSS-Utils

一个独立，可扩展的css基础模块集合。

## 目录说明

**mixins**: 包含一些常用的mixin，调用方式如：`@include m-opacity(.5)`，主要包含如下类：

```scss
// a链接样式设置
@mixin m-link($link-color,$link-hover-color:darken($link-color,5%)){...}
// 设置该类下所有子元素的font-family值
@mixin m-font-family($ff){...}
// 设置该类下所有子元素的font-size属性
// 基本的font-size为`$fz`
// 标题的`font-size`为`$hfz`
@mixin m-font-size($fz,$hfz){...}
// 设置border-radius
@mixin m-border-radius($radius) {...}
// 设置opacity
@mixin m-opacity($opacity) {...}
// 设置多行显示省略号
@mixin m-text-ellipsis($line-number) {...}  
```

**base**: 包含一些跟文字，颜色，链接等相关的基本样式类，样式变量参考根目录下文件`var.scss`，主要包含如下类：

```scss
// font-family样式设置
.ff--apple {@include m-font-family($ff-apple);}
.ff--helvetica {@include m-font-family($ff-helvetica);}
.ff--noto {@include m-font-family($ff-noto);}
.ff--yahei {@include m-font-family($ff-yahei);}
// font-size样式设置
.fz--primary {@include m-font-size($base-size,$base-h-sizes);}
// link链接设置
.link--primary {@include m-link($base-primary-color);}
```

**func**: 单值属性函数，可以快速调用对应属性与所搭配的常用属性值，包含的部分类如下所示：

```scss
// position位置控制
.f-pr{position: relative;}
.f-pa{position: absolute;}
.f-pf{position: fixed;}
// float清除浮动
.f-fl{float: left;}
.f-fr{float: right;}
```

**unit**: 多值属性单元，可以快速调用对应单元完成一个独立的功能，主要包含如下类：

```scss
// 图像成比例缩放
.u-imgr{...}
// 清除浮动
.u-clearfloat {...}
// 单行文本的溢出显示省略号
.u-text-ellipsis {...}
// 自定义滑动bar
.u-scrollbar--style1 {...}
```

**grid**: 用于自适应布局的网格类，其使用例子如：

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

**reset**: 包含一些常用的重置浏览器默认样式的类，文件介绍如下：

  - reset: 包含一些常用重置类。
  - normalize: 外部通用重置类，具体可见[normalize官网](https://necolas.github.io/normalize.css/)。

## 注意

- 每一个类文件应该引用独立，负责自己需要引用的类。
- 任何直接依赖`var.scss`的类均使用`-r`后缀。
- `_export.scss`用于可在外部引用的基本类。