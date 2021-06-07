# Charts

Charts are prefered in displaying data analysis. The most common types of them are:
1. Pie chart
2. Bar chart
3. Line chart 

## Setting up charts

You need to download chart folder, unzip it and lin it to the html folder through the script.

When building line, pie, or bar chart, canvas element is used, then you initiate the chart.
In line chart and bar chart provided in an object, labels and data. While in pie chart we provide the values with their colors. 

3 attributes can be added **optionally** in canvas: width, height, and id.

## Rectangules drawing 
We can use the follong functions to draw recatangles:
1. fillRect 2, strokeRect 3. clearRect

## Drawing paths
1. Create a path (beginPath()) 2. Use **drawing commands** 3. Use path methods (closepath(), stroke(), fill()). 

**moveTo()** function id important in drawing paths, it's like pens.
**lineTO'()** starting line depends on previousl drawn path
**arc()** has 6 parameters: x, y , the center of the circle, start angle, end angle, and radius.
