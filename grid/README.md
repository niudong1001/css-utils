# Grid网格类

用于自适应布局的网格类。

## 主要类介绍

- `g-row`: 所有`g-col-*`的父类，代表一行。
- `g-col`: 所有单列都必须包含的基础类。
- `g-col-$i`: 一个单列，宽度为`$i/$total-columns`。
- `g-col-$bpname-$i`: 一个响应式单列，宽度为`$i/$total-columns`。
- `g-offset-$i`: 控制一个单列的`margin-left=$i/$total-columns`。
- `g-offset-$bpname-$i`: 控制一个响应式单列的`margin-left=$i/$total-columns`。

> 上面`$bpname`可能取`$bp-maps`中的值。  
> 上面`$i`的范围为`[1, $total-columns-1]`。

## 使用例子

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

## 注意

> 布局使用了float方式。  
> 建议所有`g-col-*`中包含子对象div后进行操作，这样避免padding与background带来的一些问题。
> 可以使用`test.html`来验证类效果。