![](https://cdnp3.stackassets.com/1f9afe93437a36a0e82ca18ba25a5e0e866a1de0/store/31db3fecd4649bf094fa02b5552cdb5730f332822218d8b778f333c8e82e/f9307202ca774a92107cdb0e6f831e25b9570643_main_hero_image.jpg)

# Canvas

## Basic usage of canvas

The `<canvas>` element

```
<canvas id="tutorial" width="150" height="150"></canvas>
```

The HTML `<canvas>` tag is used to draw graphics, on the fly, via scripting (usually JavaScript).
HTML5 element `<canvas>` gives you an easy and powerful way to draw graphics using JavaScript. It can be used to draw graphs, make photo compositions or do simple (and not so simple) animations.

```
<canvas id = "mycanvas" width = "100" height = "100"></canvas>
```

You can easily find that `<canvas>` element in the DOM using getElementById() method as follows −

```
var canvas = document.getElementById("mycanvas");
```

```
<!DOCTYPE HTML>

<html>
   <head>
   
      <style>
         #mycanvas{border:1px solid red;}
      </style>
   </head>
   
   <body>
      <canvas id = "mycanvas" width = "100" height = "100"></canvas>
   </body>
</html>
```

![](https://s16458.pcdn.co/wp-content/uploads/images/u6/pdfgeneratorsdk_js_pdf_draw_rectangle.png)

### HTML5 Canvas Examples

| Sr. No.  |  Examples & Description |
|---|---|
| 1  | Drawing Rectangles Learn how to draw rectangle using HTML5 `<canvas>` element  |
| 2  |  2	Drawing Paths Learn how to make shapes using paths in HTML5 `<canvas>` element |
| 3  | Drawing Lines Learn how to draw lines using HTML5 `<canvas>` element  |
| 4  | Drawing Bezier Learn how to draw Bezier curve using HTML5 `<canvas>` element  |
| 5  |  Drawing Quadratic Learn how to draw quadratic curve using HTML5 `<canvas>` element |
| 6  |  Using Images Learn how to use images with HTML5 `<canvas>` element |
| 7  | Create Gradients Learn how to create gradients using HTML5 `<canvas>` element  |
| 8  |  Styles and Colors Learn how to apply styles and colors using HTML5 `<canvas>` element |
| 9  |  Text and Fonts Learn how to draw amazing text using different fonts and their size. |
| 10  |  Pattern and Shadow Learn how to draw different patterns and drop shadows. |
| 11  |  Canvas States Learn how to save and restore canvas states while doing complex drawings on a canvas. |
| 12  |  Canvas Translation This method is used to move the canvas and its origin to a different point in the grid. |
| 13  |  Canvas Rotation This method is used to rotate the canvas around the current origin. |
| 14 |  Canvas Scaling This method is used to increase or decrease the units in a canvas grid. |
| 15 |  Canvas Transform These methods allow modifications directly to the transformation matrix.. |
| 16 |  Canvas Composition This method is used to mask off certain areas or clear sections from the canvas. |
| 17 |  Canvas Animation Learn how to create basic animation using HTML5 canvas and JavaScript. |


![](https://www.researchgate.net/profile/Curran_Kelleher/publication/262398551/figure/fig5/AS:666687049306144@1535961987543/Example-code-for-HTML5-Canvas.png)


```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
     var ctx = canvas.getContext('2d');

    ctx.beginPath();
    ctx.arc(75, 75, 50, 0, Math.PI * 2, true); // Outer circle
    ctx.moveTo(110, 75);
    ctx.arc(75, 75, 35, 0, Math.PI, false);  // Mouth (clockwise)
    ctx.moveTo(65, 65);
    ctx.arc(60, 65, 5, 0, Math.PI * 2, true);  // Left eye
    ctx.moveTo(95, 65);
    ctx.arc(90, 65, 5, 0, Math.PI * 2, true);  // Right eye
    ctx.stroke();
  }
}
```

![](https://mdn.mozillademos.org/files/252/Canvas_smiley.png)


![](https://i.ytimg.com/vi/AcoUu3bgKgM/maxresdefault.jpg)

# Chart.js

Chart.js can be used with ES6 modules, plain JavaScript and module loaders.

## Creating a Chart
It's easy to get started with Chart.js. All that's required is the script included in your page along with a single `<canvas>` node to render the chart.


```
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
});
</script>

```

![](https://cdn.mos.cms.futurecdn.net/S5bicwPe8vbP9nt3iwAwwi.jpg)

## Accessible Charts

Chart.js charts are rendered on user provided canvas elements. Thus, it is up to the user to create the canvas element in a way that is accessible. The canvas element has support in all browsers and will render on screen but the canvas content will not be accessible to screen readers.


By setting the `role` and `aria-label`, this `canvas` now has an accessible name.

```
<canvas id="goodCanvas1" width="400" height="100" aria-label="Hello ARIA World" role="img"></canvas>
```

This `canvas` element has a text alternative via fallback content.

```
<canvas id="okCanvas2" width="400" height="100">
    <p>Hello Fallback World</p>
</canvas>
```


## Chart type
1. Line
2. Bar
3. Radar
4. Doughnut and Pie
5. Polar area
6. Bubble
7. Scatter


### Line 
![](https://cdn.wallstreetmojo.com/wp-content/uploads/2019/04/Line-Chart-Examples.png)

### Bar 
![](https://chartio.com/assets/dfd59f/tutorials/charts/grouped-bar-charts/c1fde6017511bbef7ba9bb245a113c07f8ff32173a7c0d742a4e1eac1930a3c5/grouped-bar-example-1.png)

### Radar 
![](https://www.researchgate.net/profile/Astrid_Buica/publication/327746307/figure/fig4/AS:672559683084291@1537362132393/Spider-web-plot-showing-the-aromatic-profile-of-the-combinations-DA-samples-including.png)

### Doughnut and Pie 
![](https://www.amcharts.com/wp-content/uploads/2013/11/demo_129_none.png)

### Polar area 
![](https://pnp.github.io/sp-dev-fx-controls-react/assets/PolarAreaChart.png)

### Bubble 
![](https://d2slcw3kip6qmk.cloudfront.net/marketing/blog/2017Q4/how-to-make-a-bubble-chart-in-excel/bubble-chart-template.png)

### Scatter 
![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Scatter_diagram_for_quality_characteristic_XXX.svg/1200px-Scatter_diagram_for_quality_characteristic_XXX.svg.png)