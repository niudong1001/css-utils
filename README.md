# CSS-Utils

一个简洁，独立，可扩展的css基础模块集合。本仓库只包含基本的函数类或辅助类，不包含更高级别的UI定制模块，您可以使用导入特定的模块文件实现只引用该类。

## 目录说明

- [Mixins混合函数](./mixins/mixins.scss)：本模块包含一些常用的**Mixin混合函数**，调用方式为`@include m-opacity(.5)`，其包含的类与其功能说明如下所示:

```scss
// 链接样式类函数
@mixin m-link($link-color,$link-hover-color:darken($link-color,5%)){...}

// 设置该类下所有子元素的font-family属性
@mixin m-font-family($ff){...}

// 设置该类下所有子元素的font-size属性
// 设置基本的font-size为'$fz'
// 设置标题的font-size为'$hfz'
@mixin m-font-size($fz,$hfz){...}

// 设置border-radius
@mixin m-border-radius($radius) {...}

// 设置opacity
@mixin m-opacity($opacity) {...}

// 设置多行显示省略号，'$line-number'为行数
@mixin m-text-ellipsis($line-number) {...}  
```

- [Base基本样式](./base/base-r.scss)：本模块包含一些跟**文字**，**颜色**，**链接**等相关的基本样式类，样式变量参考根目录下文件`var.scss`，包含类与其功能说明如下所示：

```scss
// font-family样式设置
.ff--apple {@include m-font-family($ff-apple);}
.ff--helvetica {@include m-font-family($ff-helvetica);}
.ff--noto {@include m-font-family($ff-noto);}
.ff--yahei {@include m-font-family($ff-yahei);}

// font-size样式设置
.fz--primary {@include m-font-size($base-size,$base-h-sizes);}

// link链接设置
.link--primary {@include m-link($base-primary-color);}
```

- **Func单值属性函数**：本模块包含常见的**单值属性函数**，可以快速调用对应属性与所搭配的常用属性值，包含的文件包括：

  - [静态单值属性函数](./func/func.scss)：不依赖`var.scss`。
  - [动态单值属性函数](./func/func-r.scss)：依赖`var.scss`。

  包含的部分类与其功能说明如下所示:

```scss
// position位置控制
.f-pr{position: relative;}
.f-pa{position: absolute;}
.f-pf{position: fixed;}

// float清除浮动
.f-fl{float: left;}
.f-fr{float: right;}
```

- [Unit多值属性单元](./unit/unit.scss)：本模块包含常用的**多值属性单元**，可以快速调用对应单元模块完成一个独立的功能，包含类与其功能说明如下所示:

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

- [Grid网格布局](./grid/grid-r.scss)：本模块包含常用的自适应网格布局功能，其采用float属性来实现，使用例子如下：

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

- [Reset重置默认类](./reset/reset.scss)：本模块包含一些常用的重置浏览器默认样式的类，如：

```scss
// 基本重置类
.reset--primary {
  body {margin: 0;}
  input,button,select,textarea{outline:none;}
}
```

## 注意

- 每一个类文件应该**引用独立**，负责自己需要引用的类。
- 任何直接依赖`var.scss`的类均使用`-r`后缀。
- `_export.scss`用于可在外部引用的基本类。
