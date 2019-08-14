# d3-radial

D3 plugin allowing to create radial bar chart from a flat data set.

The plugin aims to follow the convention for developing D3 plugins described in [Towards Reusable Charts](https://bost.ocks.org/mike/chart/) by Mike Bostock.

![Example01](https://github.com/ksokolovic/d3-radial/blob/develop/Image/example%20image.png)
<!-- The example address has not been changed -->

## Installing

If you are using NPM, you can install the plugin via:

```sh
$ npm install d3-radial
```

Otherwise, download the [latest release](https://github.com/ksokolovic/d3-pivots/releases/latest) and include it in your page using the `script` tag.   
<!-- the address has not been changed. -->

### Dependencies

The plugin depends on the [Underscore](https://underscorejs.org/) JavaScript library. Hence, it must also be included in the `script` tag of your page.
<!-- Not sure how to change the dependencies -->


```html
<script src="../build/d3-pivots.min.js"></script>
<script src="https://d3js.org/d3.v4.js"></script>

<!-- Don't forget to include underscore.js -->
<script src="assets/js/underscore-min.js"></script>
```

## Examples

Check out the `examples/example.html` to see the plugin in practice. 

Below is listed the snippet that's used for initializing the radial bar chart with the sample data set:

```js
let data = [ 
          {key: 'JavaScript', value: 2300000}, 
          {key: 'Python', value: 1000000}, 
          {key: 'Java', value: 986000}, 
          {key: 'Ruby', value: 870000}, 
          {key: 'PHP', value: 559000}
        ];
          

        let radialChart = d3.radialChart()
          .data(data)
          .arcPadding(15)
          .max(3000000)
          .round(15);

        d3.select('#radial-chart')
          .call(radialChart);
```

## API Reference

### d3.radialChart()

Initializes and returns a new radial bar `chart` instance.

### chart.width([width])

Sets or returns the width of the chart.

### chart.height([height])

Sets or returns the height of the chart.

### chart.margin([margin])

Sets or returns the margins of the chart.

`margin` is an object that has the following format and default values: 

```js
{top: 10, right: 25, bottom: 10, left: 25}
```

### chart.textSize([textSize])

Set or return the size of text to be rendered on the chart.

### chart.arcPadding([arcPadding])

Set or return the padding between adjacent bar chart.

### chart.colors([colors])

Sets or returns the color palette to use for rendering chart. 

The palette has the form of an array of hex color values. By default, the chart is initialized with the palette of random colors.

### chart.backgroundArcColor([backgroundArcColor])

Set or return the color of background arc on the chart.

### chart.lineColor([lineColor])

Set or return the color of the line between the lable and the chart.

### chart.data([data])

Sets or returns the data to be rendered on the chart.

### chart.pointValue([pointValue])

Set or return the value of each category on the chart.

### chart.pointKey([pointKey])

Set or return the text of each category on the chart.

### chart.max([max])

Set or return the max value of the background arc on the chart.

### chart.round([round])

If radius is specified, sets the corner radius to the specified function or number and returns this arc generator.

If radius is not specified, returns false which will make the egde to be right angle.

## Authors

 Name                | E-mail address            | Skype ID
:-------------------:|---------------------------|-----------------------
 Kemal Sokolović     | kemal.sokolovic@gmail.com | kemal.sokolovic
 Shuxi Lian          | sxliam223@gmail.com       | live:b5373e636fec6e95

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) for details.