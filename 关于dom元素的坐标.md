

> https://javascript.info/size-and-scroll#sample-element

# Element size and scrolling

There are many JavaScript properties that allow to read information about element width, height and other geometry features.

我们有很多可以获取元素宽高和其他的集合属性。

We often need them when moving or positioning elements in JavaScript, to correctly calculate coordinates.

我们经常需要通过这些属性，移动元素、定位元素、正确计算元素的坐标
# Sample element 实例

As a sample element to demonstrate properties we’ll use the one given below:

例如下面的例子，我们将展示相关的属性

``` html
<div id="example">
  ...Text...
</div>
<style>
  #example {
    width: 300px;
    height: 200px;
    border: 25px solid #E8C48F;
    padding: 20px;
    overflow: auto;
  }
</style>
```

It has the border, padding and scrolling. The full set of features. There are no margins, as they are not the part of the element itself, and there are no special properties for them.

这个元素boder panding scrolling。几乎是所有的属性。没有margin，因为他不是元素自身的一部分.

The element looks like this: 元素如下所示：

![dfasdfasdfasdf](https://javascript.info/article/size-and-scroll/metric-css.png)

## Geometry

Element properties that provide width, height and other geometry are always numbers. They are assumed to be in pixels.

Here’s the overall picture:

![dfadfasdfadf](https://javascript.info/article/size-and-scroll/metric-all.png)

They are many properties, it’s difficult to fit them all in the single picture, but their values are simple and easy to understand.

Let’s start exploring them from the outside of the element.

## offsetParent, offsetLeft/Top

These properties are rarely needed, but still they are the “most outer” geometry properties, so we’ll start with them.

In the example below the inner <div> has <main> as offsetParent and offsetLeft/offsetTop are shifts from its left-upper corner (180):

``` html
<main style="position: relative" id="main">
  <article>
    <div id="example" style="position: absolute; left: 180px; top: 180px">...</div>
  </article>
</main>
<script>
  alert(example.offsetParent.id); // main
  alert(example.offsetLeft); // 180 (note: a number, not a string "180px")
  alert(example.offsetTop); // 180
</script>
```

![ccccc](https://javascript.info/article/size-and-scroll/metric-offset-parent.png)