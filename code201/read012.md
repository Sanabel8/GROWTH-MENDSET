charts
* Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool
* JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.
* The first thing we need to do is download Chart.js. 
```<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```
* for drawing aline chart :
1. add to the body of html ```<canvas id="buyers" width="600" height="400"></canvas>```
2. add in the foot of body 
```<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>```


3.Inside the same script tags we need to create our data,above aline var buyers= we should add

```var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
```

4. If you test your file in a browser you’ll now see a cool animated line graph.

* drowing a pie chart:
1. canves elemen ```<canvas id="countries" width="600" height="400"></canvas>```
2. Next, we need to get the context and to instantiate the chart:
```var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);
```
3. create the data like value and color :
```var pieData = [
	{
		value: 20,
		color:"#878BB6"
	},
	{
		value : 40,
		color : "#4ACAB4"
	},
	{
		value : 10,
		color : "#FF8153"
	},
	{
		value : 30,
		color : "#FFEA88"
	}
];
```
4. after that add options:```var pieOptions = {
	segmentShowStroke : false,
	animateScale : true
}```

* drawing bar chart:
1. added canvas element```<canvas id="income" width="600" height="400"></canvas>```
2. retrieve the element and create the graph:
```var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);
```
3 . add data like aline chart.

* canvas
1.The ```<canvas>``` element creates a fixed-size drawing surface that exposes one or more rendering contexts
2. you can access the drawing context using its getContext() method.
3.  There are three functions that draw rectangles on the canvas:
. fillRect(x, y, width, height) :Draws a filled rectangle.
. strokeRect(x, y, width, height) :Draws a rectangular outline.
. clearRect(x, y, width, height) :Clears the specified rectangular area, making it fully transparent.

* Styling text:
1.font = value
2.textAlign = value
3.textBaseline = value
4.direction = value






























