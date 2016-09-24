---
layout: post
title: Exploring Javascript Chart Libraries, Getting started with Chart.js.
excerpt: Come along as we learn to make some charts with chart.js.
permalink: /getting-started-with-chartjs
smlogo: Chartjs.png
---

<div class="text-center"><img src="http://www.chartjs.org/img/chartjs-logo.svg"></div>
<br />

I recently got a request for developing a chart based front end, it got me excited about chart libraries and other chart based projects, so I'd like to explore [chart.js ](http://www.chartjs.org){:target="_blank"} a popular open source charting library, come along as we learn how to make some charts !

*Note: I'll be using codepen (free and awesome) and gave myself little challenges you are welcome to try if you want to recreate my own learning curve.*


> My/Your challenge: Import Chart.js,add and configure a simple chart that is not one of their examples.

<p data-height="460" data-theme-id="0" data-slug-hash="oLVvoN" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/oLVvoN/">Chart.js My First Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


It took a bit of hammering out, so if you didn't succeed at first don't fret, this is what I learned:

- Chart.js is canvas based (as opposed to SVG). So your HTML is minimal, just a canvas tag.

- Relies heavily on nested Arrays & Objects to configure ( see the Js file for a subdivison of global option, chart options and data ), and a good knowledge of the documentation to look at all the features and options.

- Use a container or css grid ( I am using Bootstrap) to simplify displaying the chart.

Alright, I have a basic understanding of Chart.js, lets try some of the different types of charts and see what we can learn:

> My/Your challenge: Make a bar chart with chart.js

<p data-height="460" data-theme-id="0" data-slug-hash="EyrXyx" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EyrXyx/">Chart.js Bar Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


Still experimenting with the  best way to declare the chart and adding options, I think it reads a little better if you divide global options, dataset and chart options rather than have them all in the chart declaration, but a bar chart was made , on to a pie chart.

> My/Your challenge: Make a pie chart with chart.js

<p data-height="460" data-theme-id="0" data-slug-hash="dXAQOp" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/dXAQOp/">Chart.js Pie Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Success! another chart full of insight, for this one I only changed some minor options (Removed the background, rotated the chart & added some borders) , the trick is going over the documentation for the specific chart; in this case the [Pie & Doughnut](http://www.chartjs.org/docs/#doughnut-pie-chart){:target="_blank"} and finding the feature you want to add,remove or modify.

Ok, Let's revisit the line chart and try multiple data series and more options.


> My/Your challenge: Make a line chart with multple data series, go crazy with the options

<p data-height="460" data-theme-id="0" data-slug-hash="pbYGVa" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/pbYGVa/">Chart.js Line Chart Multiple Series</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

- I learned that the trick for multiple series, is just to add an extra data element to the dataset object, or multiple if you have more, check the code.
- Each dataset has it's own options, so you can format each line in a different way, and finally, I added a label to the Yaxis.
- It might not be apparent, but you can interact with the chart in a number of ways, you can click the labels and hide the data series, and hover and click on the chart to call other functions.

One last thing I would like to explore, is changing the chart once it is displayed through javascript, something I believe can come in handy in a production environment.

> My/Your challenge: Interact with a chart and change it's configuration or dataset

<p data-height="510" data-theme-id="0" data-slug-hash="zBXqYR" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/zBXqYR/">Chart.js Toggle Chart </a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Chart.js can be modified to your hearts content by rebuilding the chart  and redrawing the canvas, a common method if you've ever worked with the canvas in html5, as mentioned above, this is just an introduction, but check the [advanced usage in the docs](http://www.chartjs.org/docs/#advanced-usage){:target="_blank"}.

I'll end up this short introduction to chart.js by saying that working with the library was mostly a joy and I hope these few pens help you get started.

Best,

Keno
