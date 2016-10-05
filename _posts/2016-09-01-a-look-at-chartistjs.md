---
layout: post
title: A look at Chartist.js with sample code
excerpt: A quick introduction to Chartist.js a SVG javascript chart library, come do some charts !
permalink: /a-look-at-chartist
smlogo: chartist.png
---

<h1>CHARTIST.JS</h1>

![chartist](assets/images/chartist-guy.gif){:class="img-responsive"}

I recently wrote about [chartJS (go check it out !)]({{ site.baseurl }}/getting-started-with-chartjs) a pretty cool javascript charting library; I would like to explore a few more charting libraries and I've had my eye on chartist.js for a while.

So come along as we learn how to make charts with [CHARTIST.JS](https://gionkunz.github.io/chartist-js/){:target="_blank"}

<i>Note: I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</i>


>Challenge: Import chartist.js and create a chart, any chart.

<p data-height="360" data-theme-id="0" data-slug-hash="XjAJOA" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/XjAJOA/">Chartist.js First Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Success! I learned that to make a chart in **Chartist**, a minimal example needs a container and a chart declaration in javascript, the default styles are defined within css ( more on that later ) and it is SVG based  ( unlike Chart.js which is Canvas based ).

<h3>Aspect Ratios</h3>

One thing the documentation makes emphasis on, is the display of chart containers through aspect ratios, [check the documentation](https://gionkunz.github.io/chartist-js/getting-started.html){:target="_blank"}.

> Challenge : Display a chart with different Aspect Ratios

<p data-height="360" data-theme-id="0" data-slug-hash="qaWdjm" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/qaWdjm/">Chartist.js Aspect Ratios</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Rather than do one example, I cooked up an interactive way for you to check out **ALL** the aspect ratios Chartists supports, using them is just a matter of adding them to your chart container like so:

   <pre>&lt;div id="chart" class="ct-chart ct-golden-section"&gt;&lt;/div&gt;</pre>


<h3>Chart Options</h3>

So what kind of options does chartist provide ? le's find out:

> Challenge : Make a line chart with options

<p data-height="360" data-theme-id="0" data-slug-hash="jrNGBR" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/jrNGBR/">Chartist.js Options</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
I found out 2 key things about options in chartist:

- You can add them as a variable object to the chart configuration, and...
- The options for the specific charts are found on the documentation, I should caution that they are somehow hidden under the a code button for every chart.


<h3>Style Options</h3>

And what about style options,  chartist seems to  isolate and treat the style options within CSS, so let's explore that:

>Challenge : Change the style of a chart with CSS

<p data-height="360" data-theme-id="0" data-slug-hash="vXBpAX" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vXBpAX/">Chartist.js CSS Styles & Series Labels</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Chartist makes it super easy to style the basics of your chart, things like line color and data-points (you can apply them to the whole chart or individually to a data series), for everything else you are going to write some CSS or hope [there is already a plugin](https://gionkunz.github.io/chartist-js/plugins.html){:target="_blank"} that does what you want, in this case, I really wanted labels for both series and specific background colors for the whole chart, you can probably use divs instead of SVG shapes like I did.

<h3>More Chart Types</h3>

Let's explore the other chart types that chartist provides before coming back to plugins:

   > Challenge: create a pie and a donut chart  

   <p data-height="600" data-theme-id="0" data-slug-hash="EgYEVw" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EgYEVw/">Chartist.js Pie & Donut Charts</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
   <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Using the bits we explored before, it is relatively easy to add pie and donut charts.  

<h3>Plugins:</h3>

As mentioned before, chartist allows for added functionality via plugins, let's try that.

> Challenge: Add at least 2 plugins to a chart  

<p data-height="360" data-theme-id="0" data-slug-hash="WGZVdX" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WGZVdX/">Chartist.js Plugins</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<i>Note: The above chart adds Axis titles and data label plugins</i>

Chartist insist in a strict differentiation of data and style, so a few things like labels and axis titles need to be added with [plugins](https://gionkunz.github.io/chartist-js/plugins.html){:target="_blank"}, the upside being that it is super small and efficient,You can add multiple [plugins](https://gionkunz.github.io/chartist-js/plugins.html){:target="_blank"} by first linking the scripts after chartist, and then adding them along with their options to your chart declaration.


> Things I didn't cover/further challenges: Animating charts & making your own plugins, integration with web frameworks (like angular & react)

<h3>The Takeaway:</h3>

I loved working with chartist.js, it is easy and fun to get started and some of its decisions make a lot of sense ( separating style and data) , my biggest takeaway though, is that chartist is both easy and fast at first, but you will have to code both in CSS and JS if you need something else, which depending on your project might be exactly what you need or not at all.

Best,

Keno
