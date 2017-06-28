# ChartsLab-Geometry

Visualizations typically consist of discrete graphical Geometries, such as [symbols](#symbols), [arcs](#arcs), [lines](#lines) and [areas](#areas), [bars](#bar), [pie](#pie). This module provides a variety of shape generators for your convenience, and easy to use in **HTML5_Canvas**

## Install
You can install this micro-library by download the latest version or by downloading the full bundle [ChartsLab](https://github.com/ChartsLab/) library.

```html
<script src="./Geometry.js"></script>
```

## Requires
This micro-library requires [Scales](https://github.com/ChartsLab/ChartsLab-Scale) for data encoding and you can use [Stat](https://github.com/ChartsLab/) or/and [Filter](https://github.com/ChartsLab/) for easy and simple data entry


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

  Arc is the general shape/geometry naming of many plotting shapes like pie, daunat, coxcomb charts and these shapes are popular in data analysis and business intellegence work. And here in chartsLab we simplified bars in some API easy to use functions that you can control the plot with it.

  **Requires** Scale For data Scaling and mapping, and maybe data-filter for easy to invoke datasets.
  
  ```js
        Geometry.Arc()
            .Position([200,200])
            .Frequency(100)
            .Values([30,30,30,10])
            .Colors(['red','blue','green','yellow'])
            .Radius([50,70,20,100])
            .InnerRadius(0)
            .Centeroid(function (ctx, start, end, perc) {
                ctx.fillStyle = "#000000";
                ctx.fillText( perc,end[0], end[1]);
            })
            .Draw(context);
  ```
  
  <a name="Draw" href="#draw">#</a> Arc.<b>Draw</b>(<i> ctx **Context**</i>)
  
    This function takes canvas context and be ready for drawing in it, you maybe prepare canvas before use see [ChartCore](https://github.com/ChartsLab/) for more details. **Warn** you can't give this function any thing except canvas context or you will have raise an error for more details about errors see [ErrorHandler](https://github.com/ChartsLab/).
  
  <a name="Draw" href="#draw">#</a> Arc.<b>Draw</b>(<i> ctx **Context**</i>)
  
  <a name="Frequency" href="#frequency">#</a> Arc.<b>Frequency</b>(<i> freq **Integer**</i>)
  
  <a name="Position" href="#position">#</a> Arc.<b>Position</b>(<i>[StartPoint **Array**], [EndPoint **Array**]</i>)
  
  <a name="Radius" href="#radius">#</a> Arc.<b>Radius</b>(<i> rad **Integer**</i>)
  
  <a name="InnerRadius" href="#innerRadius">#</a> Arc.<b>InnerRadius</b>(<i> rad **Integer**</i>)
  
  <a name="Values" href="#values">#</a> Arc.<b>Values</b>(<i>[dataValues **Array**]</i>)
  
  <a name="Colors" href="#colors">#</a> Arc.<b>Colors</b>(<i>[colorsValues **Array**]</i>)
  
  <a name="Centeroid" href="#centeroid">#</a> Arc.<b>Centeroid</b>(<i> funcCallback **Function**</i>)
    
* [Areas](#areas)
* [Bars](#bars)

  Bars(Intervals) is one of common-used plots and primitives in data visualization. And here in chartsLab we simplified bars in some API easy to use functions that you can control the plot with it.

  **Requires** Scale For data Scaling and mapping, and maybe data-filter for easy to invoke datasets.

  ```js
        Geometry.Bar.
                .xScale(x)
                .yScale(y)
                .xVector(xVec)
                .yVector(yVec)
                .Draw(ctx);
  ```

  <a name="Draw" href="#draw">#</a> Bar.<b>Draw</b>(<i> ctx **Context**</i>)
  
    This function takes canvas context and be ready for drawing in it, you maybe prepare canvas before use see [ChartCore](https://github.com/ChartsLab/) for more details. **Warn** you can't give this function any thing except canvas context or you will have raise an error for more details about errors see [ErrorHandler](https://github.com/ChartsLab/).
    
  <a name="Size" href="#size">#</a> Bar.<b>Size</b>(<i>Size **Integer**</i>)
  
    Size Take an Integer Positive value for all Bars sizes(width), you can customize it be a column histogram see [Column](#column)
  
  <a name="Position" href="#position">#</a> Bar.<b>Position</b>(<i>[StartPoint **Array**], [EndPoint **Array**]</i>)
  
    Position Take 2 Array each contain 2 value for start and end coordinates, you can control the position of start you Bar chart from here (But not the axis see [Axis](https://github.com/ChartsLab/ChartsLab-Axis/))
  
  <a name="xScale" href="#xscale">#</a> Bar.<b>xScale</b>(<i>y **Scale**</i>)
  
    Scale(X) is the mapping function that maps each bar to certain position along X Axis based on it's X value, see [Scale](https://github.com/ChartsLab/ChartsLab-Scale/) for more details, this function simpilify for you to find the position and this is the only required class need for Bar plots.

  <a name="yScale" href="#yscale">#</a> Bar.<b>yScale</b>(<i>x **Scale**</i>)
  
    Scale(Y) is the mapping function that maps each bar to certain position along Y Axis based on it's Y value, see [Scale](https://github.com/ChartsLab/ChartsLab-Scale/) for more details, this function simpilify for you to find the position and this is the only required class need for Bar plots.

  <a name="xVector" href="#xvector">#</a> Bar.<b>xVector</b>(<i>Vector **Vector**</i>)
    
    Vector(X) is taking a vector that represent the bars X values, **Warn** if you tried to pass an array this function will raise and error see [ErrorHandler](https://github.com/ChartsLab/), you can use [Data-Filter](https://github.com/ChartsLab/) for more details, but it's not required actually, you can manipulate any array to work with it but it's easlt to use [Data-Filter](https://github.com/ChartsLab/).

  <a name="yVector" href="#yvector">#</a> Bar.<b>yVector</b>(<i>Vector **Vector**</i>)
  
    Vector(Y) is taking a vector that represent the bars Y values, **Warn** if you tried to pass an array this function will raise and error see [ErrorHandler](https://github.com/ChartsLab/), you can use [Data-Filter](https://github.com/ChartsLab/) for more details, but it's not required actually, you can manipulate any array to work with it but it's easlt to use [Data-Filter](https://github.com/ChartsLab/).
  
  <a name="Column" href="#column">#</a> Bar.<b>Column</b>(<i>flag **Boolean**</i>)
  
    Column is simple function that's ask you to choose a column bar or row one, it's for simplicity but you can use rotation see [ChartCore](https://github.com/ChartsLab/) for more details in this topic

  <a name="Colors" href="#colors">#</a> Bar.<b>Colors</b>(<i>mu **Scale**</i>)
    
    Scale(mu) is the mapping function that maps each bar to certain color gradiant, see [Color-Scale](https://github.com/ChartsLab/ChartsLab-Scale/) for more details, this function simpilify for you to find the color and this is the only required class need for Bar plots.
  
* [Curves](#curves)
* [Custom Curves](#custom-curves)
* [Custom Symbol Types](#custom-symbol-types)
* [Lines](#lines)
* [Pies](#pies)
* [Stacks](#stacks)
* [Symbols](#symbols)
