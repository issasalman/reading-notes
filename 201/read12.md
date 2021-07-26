## what is Chart.js?

Chart.js is a community maintained open-source library (it’s available on GitHub) that helps you easily visualize data using JavaScript. It’s similar to Chartist and Google Charts. It supports 8 different chart types (including bars, lines, & pies), and they’re all responsive. In other words, you set up your chart once, and Chart.js will do the heavy-lifting for you and make sure that it’s always legible (for example by removing some uncritical details if the chart gets smaller).

![chart](https://www.chartjs.org/media/logo-title.svg)

### How to  draw a chart with Chart.js:
1. Define where on your page to draw the graph.
2. Define what type of graph you want to draw.
3. Supply Chart.js with data, labels, and other options.

### advantages of charts
* They’re easier to look at and convey data quickly, but they’re not always easy to create.


* The great things about Chart.js are that it’s simple to use and really very flexible

### setting up  and drawing  line chart
The first thing we need to do is download Chart.js. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:



    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    <canvas id="buyers" width="600" height="400"></canvas>
    <script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);


    var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]</script> </body>`
}
![chart](https://res.cloudinary.com/practicaldev/image/fetch/s--Tmx9gqIx--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://i2.wp.com/blogreact.com/wp-content/uploads/2020/06/charts.png%3Ffit%3D750%252C398%26ssl%3D1)

### Chart Types
1. line chart
2. Bar chart
3. Radar chart
4. Doughnut and Pie Charts   
5. Polar Area Chart
6. Bubble Chart
7. catter Chart
8. Area Chart
9. Mixed Chart Types



## canvas api
<canvas is an HTML element which can be used to draw graphics via scripting (usually JavaScript). This can, for instance, be used to draw graphs, combine photos, or create simple (and not so simple) animations. The images on this page show examples of <canvas implementations which will be created in this tutorial.

This tutorial describes how to use the <canvas element to draw 2D graphics, starting with the basics. The examples provided should give you some clear ideas about what you can do with canvas, and will provide code snippets that may get you started in building your own content.

First introduced in WebKit by Apple for the OS X Dashboard, <canvas has since been implemented in browsers. Today, all major browsers support it.


### Drawing text
![text](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/html-graphics-canvas/Images/can-text.png)
The canvas rendering context provides two methods to render text:

* fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
* strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

A fillText example

The text is filled using the current fillStyle.

`
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}`



