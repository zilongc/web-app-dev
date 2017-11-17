# Element size and scrolling

There are many JavaScript properties that allow to read information about element width, height and other geometry features.

We often need them when moving or positioning elements in JavaScript, to correctly calculate coordinates.
# Sample element
As a sample element to demonstrate properties we’ll use the one given below:

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

The element looks like this:

![dfasdfasdfasdf](https://javascript.info/article/size-and-scroll/metric-css.png)

## Geometry

Element properties that provide width, height and other geometry are always numbers. They are assumed to be in pixels.

Here’s the overall picture:

![dfadfasdfadf](https://javascript.info/article/size-and-scroll/metric-all.png)