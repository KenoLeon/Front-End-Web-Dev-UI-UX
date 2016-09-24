---
layout: post
title: 'A look at Javascript Chart libraries,the big one D3.js'
excerpt: D3.js is probably the best known Javascript Chart library, come check out the basics of working with the beast !
permalink: /chart-libraries-d3js
smlogo: D3.png
---

<div class="text-center"><img src={{ site.url }}"assets/images/d3Logo.png" alt="D3.js"></div>

<h3 class="fancy">Preface</h3>

<a href="https://d3js.org" target="_blank">D3.js</a> has always been a bit of a mystery to me, is it a chart library or something else ? join me in finding out with a few code samples !

<div class="challenge"> <b>Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<div class="speechBubble"><b>Shameless Plug:</b> You like charts? you like these other posts yes?
</div>



- [Getting started with Chart.js]({{ site.baseurl }}/getting-started-with-chartjs){:target="_blank"}
- [A look at Chartist.js with sample code]({{ site.baseurl }}/a-look-at-chartist){:target="_blank"}


<h3 class="fancy">Ok, Let's get started</h3>

<div class="challenge"> <b>Challenge: </b> Import D3 and create a graph or chart, any graph or chart !</div>


<p data-height="440" data-theme-id="0" data-slug-hash="ZpOxbA" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ZpOxbA/">D3.js Hello World</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Well that was interesting, it's somehow clear that D3 is not your average chart library, in their words:

<span class="quote"><span class="qBefore">&ldquo;</span>D3 allows you to bind arbitrary data to a Document Object Model (DOM), and then apply data-driven transformations to the document.<span class="qAfter">&rdquo;</span></span>

Or in layman terms: Display your data any way you like with D3, with the caveat that you will have to write your own css and javascript (albeit with the API help and framework provided by d3), a jquery for data if you will.

<div class="note"> <b>Note: </b> I am following closely the d3.js tutorial found at their site:
<a href="https://github.com/d3/d3/wiki/Tutorials" target="_blank">Tons of tutorials at d3.js</a>
</div>



<h3 class="fancy">D3 Basics</h3>

I tried making a regular bar chart, but after a few tries it became obvious I have no idea what I was doing, so I am taking a step back and figuring out D3 basics...

<div class="challenge"> <b>Challenge: </b> Figure out what the basics of binding arbitrary data to a document object model are</div>

<p data-height="543" data-theme-id="0" data-slug-hash="XjKOdN" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/XjKOdN/">D3.js Basics Binding-Appending</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Ahh, somehow clearer now( check the heavily annotated example) ; You start by creating or importing a dataset ( <span class="hl">your arbitrary data</span>) , then you select and/or create DOM elements to which you attach said data, <span class="hl">notice the dot notation</span> (short and long) which chains methods,or you could use a more verbose syntax, those seem to be the bare basics.  

<h3 class="fancy">D3 + SVG</h3>

Most tutorials seem to introduce SVG at this point, so let's try checking how svg works with D3.js

<div class="challenge"> <b>Challenge: </b> Create a chart or graph using svg and d3</div>

<div class="speechBubble"><b> Another shameless plug: </b> Not sure about SVG ? , check this other post for an introduction:
</div>

- [Getting started with SVG]({{ site.baseurl }}/Getting-Started-With-SVG){:target="_blank"}
<ul class="indented">


<p data-height="300" data-theme-id="0" data-slug-hash="vXKryx" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vXKryx/">D3.js SVG Basics</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Like in the previous example, <span class="hl">we bind data to DOM elements</span>, in this case svg rectangles, and then modify their properties with the bounded data properties. Notice also that you have to do all of the calculations for the proper display of the bars and their positioning


<h3 class="fancy"> Getting and parsing Data</h3>

There is still some ground to cover before we make a simple ( but complete ) bar or line chart, let's start with data, so far we have used simple data, but real data sources are rarely that simple.

<div class="challenge"> <b>Challenge: </b> Import date and number data in D3 and parse it.</div>

<div class="note"> <b>Note: </b> Parsing and other d3 functions have changed in the new version from a lot of previous examples, check out the changelog:
<a href="https://github.com/d3/d3/blob/master/CHANGES.md#arrays-d3-array" target="_blank">Changes in D3 4.0</a>
</div>

<br/>

<p data-height="484" data-theme-id="0" data-slug-hash="EggVBJ" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EggVBJ/">D3.js load & parse data</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

This was a little maddening because most of the examples I could find use the old syntax (read the above note), in essence after importing your data you might want to add one of the included parsers and formatters, it's actually quite simple if you follow their <a href="https://github.com/d3/d3-time-format#timeParse" target="_blank">API documentation</a>


<h3 class="fancy">Axes & Scales</h3>

The next thing a chart or graphic usually needs is axes and scales, let's figure out those next:

<div class="challenge"> <b>Challenge: </b> Display X,Y Axes for a scaled dataset with d3</div>

<p data-height="500" data-theme-id="0" data-slug-hash="qaagOA" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/qaagOA/">D3.js Axes & Scales</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Quite a few extra D3 Functions were introduced in order to make axes and labels, most of them deal with normalizing data for display, here's a quick overview :

<ul>
<li><a href="https://github.com/d3/d3-scale#continuous_domain" target="_blank">.domain</a> - Initial Range of data</li>
<li><a href="https://github.com/d3/d3-scale#continuous_range" target="_blank">.range</a> - Converted range of data ( from Thousands to 10's in this example )</li>
<li><a href="https://github.com/d3/d3-scale#linear-scales" target="_blank">ScaleLinear() or scaleTime()</a> - Which scale to use when converting</li>
<li><a href="https://github.com/d3/d3-array#extent" target="_blank">.extent</a> Min & Max range of data</li>
<li><a href="https://github.com/d3/d3-axis" target="_blank">.axisBottom() and axisLeft()</a>- Helps create axes</li>
</ul>

While It takes a little getting used to the syntax and new functions, the methodology is still the same, create elements and bind data to them.

<h3 class="fancy">A proper chart</h3>

I think I have the basics down, so now is time to bring it all together and make a proper chart, in this case I am going to try finishing the last example and add bars and lines

<div class="challenge"> <b>Challenge: </b>Create a line chart with axes,labels and scales in d3 </div>

<p data-height="500" data-theme-id="0" data-slug-hash="wzgvwb" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/wzgvwb/">D3.js Line Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

I can see a trend :)like last time, we are introducing a few functions that help us draw the line:

<ul>
<li><a href="https://github.com/d3/d3-shape/blob/master/README.md#lines" target="_blank">d3.line</a> - Creates a line with a function</li>
<li><a href="https://github.com/d3/d3-selection/blob/master/README.md#selection_datum" target="_blank">datum</a> - binds data </li>
</ul>

And what if we wanted to make the same chart as a bar chart ?

<div class="challenge"> <b>Challenge: </b> Recreate the above line chart as a bar chart</div>

<p data-height="500" data-theme-id="0" data-slug-hash="wzgvNG" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/wzgvNG/">D3.js Bar Chart</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

It is unfortunately not as simple as with other libraries, but the gist is that you need to change your domains,ranges ( for scales and proper display of information) and the html elements to represent your data, in this case svg rectangles. Additionally, you might need to use some extra functions provided by d3.js ( in this case scaleband and bandwidth) to help you finish the chart.

<div class="challenge"><b>Things I did not cover/further challenges:</b> This is just a very basic overview of D3.js; there are literally a thousand things I didn't cover, I might do another post, but in the mean time you could look into different types of charts, multiple series, responsive charts and animations</div>


<h3 class="fancy">The Takeaway</h3>

I found D3.js to be a powerful tool for displaying information,this power unfortunately comes with a steep learning curve and some other minor and not so minor pain points, an easy chart library this is not, but on the other hand, if you have complex data and are willing to learn the API, D3.js might be your best option.

<br/>
<br/>
Best,
<br/>
<br/>
Keno
