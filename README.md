# ChartsLab-Geometry

Visualizations typically consist of discrete graphical Geometries, such as [symbols](#symbols), [arcs](#arcs), [lines](#lines) and [areas](#areas), [bars](#bar), [pie](#pie). This module provides a variety of shape generators for your convenience, and easy to use in **HTML5_Canvas**

## Install
You can install this micro-library by download the latest version or by downloading the full bundle [ChartsLab](https://github.com/ChartsLab/) library.

```html
<script src="./Geometry.js"></script>
```

## Requires
This micro-library requires [Scales](https://github.com/ChartsLab/) for data encoding and you can use [Stat](https://github.com/ChartsLab/) or/and [Filter](https://github.com/ChartsLab/) for easy and simple data entry


```js
var line = Geometry.Line()
              .xScale(x)
              .yScale(y)
              .xVector(xVec)
              .yVector(yVec)
              .Draw(ctx);
```

[Try ChartsLab-Geometry in your browser.](https://github.com/ChartsLab/)

## API Reference

* [Arcs](#arcs)
* [Areas](#areas)
* [Bars](#bars)
Bars(Intervals) is one of common-used plots and primitives in data visualization. And here in chartsLab we simplified bars in some API easy to use functions that you can control the plot with it.
<a name="Draw" href="#draw">#</a> Bar.<b>Draw</b>(<i>Context</i>)
<a name="Position" href="#position">#</a> Bar.<b>Position</b>(<i>[StartPoint Array], [EndPoint Array]</i>)
* [Curves](#curves)
* [Custom Curves](#custom-curves)
* [Custom Symbol Types](#custom-symbol-types)
* [Lines](#lines)
* [Pies](#pies)
* [Stacks](#stacks)
* [Symbols](#symbols)
