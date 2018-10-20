# CSS-Utils

一个基本的，独立的，可重用，可扩展的css模块集合。

## 目录说明

- MIXINS: 一些有用的mixins，包含如：
  - `m-link($link-color,$link-hover-color:darken($link-color,5%))`: 用以设置`link`链接样式。
  - `m-ff($ff)`: 设置该类下所有子元素的`font-family`属性置为`$ff`值。
  - `m-fz($fz,$hfz)`: 设置该类下所有子元素的`font-size`属性，基本的font-size为`$fz`，标题的`font-size`为`$hfz`。

  > 使用方法为如：`@include m-fz($base-size,$base-h-sizes)`

- BASE: 包含一些跟文字，颜色，链接等相关的基本样式类，包含内容：
  - `font-family`字体颜色设置包含如：`ff--apple`, `ff--helvetica`, `ff--noto`, `ff--yahei`。
  - `font-size`字体大小设置包含如：`fz--primary`。
  - `color`字体颜色设置包含：`c--primary`。
  - `a`链接标签设置包含：`link--primary`。

  > 样式变量参考根目录下文件`var.scss`

- FUNC: 快速调用对应属性与所搭配的常用属性值，例如：

```js
/*
position位置控制
*/
.f-pr{position: relative;}
.f-pa{position: absolute;}
.f-pf{position: fixed;}
```

- GRID: 用于自适应布局的网格类，其使用例子如：

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

- BUTTON: 存储一些常用的按钮样式类别，样例如下：

```html
<button class="btn-skeleton btn-skeleton--primary">skeleton</button>
```

- RESET: 包含一些常用的重置浏览器默认样式的类，文件介绍如下：
  - reset: 包含一些常用重置类。
  - normalize: 外部通用重置类，具体可见官网。

## 撰写标准

- 每一个类文件应该引用独立，负责自己需要引用的类。
- 任何依赖`var.scss`的类使用-r后缀。
- `_export.scss`用于可在外部引用的基本类。