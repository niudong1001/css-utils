# Mixins

一些有用的mixins。

## Mixins类别

- `m-link($link-color,$link-hover-color:darken($link-color,5%))`: 用以设置`link`链接样式。
- `m-ff($ff)`: 设置该类下所有子元素的`font-family`属性置为`$ff`值。
- `m-fz($fz,$hfz)`: 设置该类下所有子元素的`font-size`属性，基本的font-size为`$fz`，标题的`font-size`为`$hfz`。

> 使用方法为如：`@include m-fz($base-size,$base-h-sizes)`