---
layout: post
title: Let's check out Material Design Lite
excerpt: Material Design is a very popular visual language and Material Design Lite is a basic and complete implementation,let's check it out.
permalink: /MaterialDesignLite
smlogo: MDL.png
---


![Material Design Lite](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/MDL.jpg)

<h3 class="fancy">Preface</h3>

I love CSS frameworks, there is a certain magic in adding a css library and a few lines of HTML and getting a polished responsive web page, so come along and check out <b>Material Design Lite</b>.

<div class="note"><b>A big note about the different Material Design Frameworks:</b>
 Material design is Google's visual language for web pages, mobile apps and more, the specifications and general information can be found here:
<ul><li><a href="https://material.io" target="_blank"><b>material.io</b></a></li></ul>

- There are multiple implementations of this language :
<ul>
    <li><a href="https://getmdl.io" target="_blank"><b>Material Design Lite: </b></a>Google sanctioned standalone implementation</li>
    <li><a href="https://material.angularjs.org/latest/" target="_blank"><b>Angular Material:</b></a> which is the open source non-google implementation for Angular</li>
    <li><a href="http://fezvrasta.github.io/bootstrap-material-design/#about" target="_blank"><b>Bootstrap Material: </b></a>A mix of css frameworks</li>
    <li><a href="http://www.material-ui.com/#/ " target="_blank"><b>Material ui: </b></a>For React</li>
    <li><a href="https://github.com/miguelcobain/ember-paper" target="_blank"><b>Ember paper</b></a> For ember.js </li>
    <li> <b>And more</b> there is probably an implementation for your favorite language out there</li>

</ul>

</div>

<div class="speechBubble"> I will be focusing on using <a href="https://getmdl.io" target="_blank"><b>Material Design Lite: </b></a> for static sites ( think portfolios,blogs,stores etc) rather than web and mobile apps, if you want to build those I've written a bit about the subject here: </div>

- [Let's try Angular Material.]({{ site.baseurl }}/lets-try-Angular-Material){:target="_blank"}
- [Integrating Angular,ChartJs and Angular Material]({{ site.baseurl }}/integrating-angularjs-chartjs){:target="_blank"}


<h3 class="fancy">Let's start by setting up</h3>

<div class="step"> <b>Step 1: </b>Import Material Design Lite and display a simple component </div>

<p data-height="400" data-theme-id="27284" data-slug-hash="ygdBqz" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - setup" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ygdBqz/">Material Design Lite - setup</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b> In order to add Material Design Lite, just include css and Js files and start adding components, in this case we are starting with a basic layout:
<code><pre> div class="mdl-layout" </pre></code>

And then adding a card component:

<code><pre> murray-card mdl-card mdl-shadow--2dp mdl-card--border </pre></code>
Notice that there are a number of options and an extra class <b>murray-card</b> you can use to customize with extra css rules.

</div>

<h3 class="fancy">Layouts & grids: </h3>

There seems to be 2 main ways of laying out a page in Material Design Lite , Layouts and Grids, let's check them both:

<div class="step"> <b>Step 2: </b>Figure out how to use layouts</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="xqKbGK" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - Layouts: Fixed Header" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xqKbGK/">Material Design Lite - Layouts: Fixed Header</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b>
Material Design layouts come in various flavors and blocks you can modify to suit your needs, most of the action happens in the first divs where you specify the layout class:
<code><pre>class="mdl-layout mdl-js-layout mdl-layout--fixed-header</pre></code>
After that it's just a matter of filling in the rest of the blocks with your content, consult the above example and the excellent documentation for more types of layouts and features: <a href="https://getmdl.io/components/index.html#layout-section" target="_blank">Material Design Lite layouts</a>

</div>

<div class="step"> <b>Step 3: </b>Figure out how to use the grid</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="yMBBQV" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - Grid" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/yMBBQV/">Material Design Lite - Grid</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b> The grid on the other hand is made with an outer container div:
<code><pre>class="mdl-grid"</pre></code> and a number of div cells <code><pre>class="mdl-cell mdl-cell--1-col"</pre></code> Cells obey a set of basic rules:<br/>

<b>A grid  has 12 columns in the desktop screen size, 8 in the tablet size, and 4 in the phone size</b>
<br/>

There are ways to change the display of cells (order, visibility column size,etc,etc) all the options are listed in the documentation:  <a href="https://getmdl.io/components/index.html#layout-section" target="_blank">Material Design Lite Grid</a>
</div>

<div class="step"> <b>Step 4: </b>Combine layouts and grids</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="LWPagv" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - Layouts,Grid & Footer" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/LWPagv/">Material Design Lite - Layouts,Grid & Footer</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<div class="explain"><b>Explanation: </b> The road to combining layouts and grids is a little bumpy, some refinements need to be made so spacing,backgrounds,margins etc,etc are to your liking, but most of these modifications can simply be made by adding a class name and adding a few CSS Rules, the components, layout and grid are pretty simple, so they play nice and are easy to customize. Notice we also added a Footer component along some cards, a transparent header, drawer and tool bar navigation, and it's all responsive.
</div>

<h3 class="fancy">Components:</h3>

Having dealt with page layout, now it's time to fill it up with some content, Material Design Lite provides a basic and complete set of options:

<a href="https://getmdl.io/components/index.html" target="_blank">Material Design Lite Components</a>


<div class="step"> <b>Step 5: </b>Include a component, any component</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="VpwdBy" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - Component" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VpwdBy/">Material Design Lite - Component</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b>While each component requires its own configuration, they are pretty much a copy/paste and modify operation, it is worth noting that they seem to be mostly geared towards <b>web content that isn’t particularly app-y.</b>(their words) , if you need something more interactive you can alwasy choose one of the other Material Design Implementations mentioned above.
</div>

<div class="step"> <b>Step 6: </b>Use multiple components</div>

<p data-height="800" data-theme-id="27284" data-slug-hash="xqxaWv" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Material Design Lite - Multiple Components" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xqxaWv/">Material Design Lite - Multiple Components</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b> Starting from a layout, it is simply a matter of adding components into a grid or various grids, each one is well documented and has a step by step process you can follow, additional modifications can be done via extra css rules.

You can also modify the color styles by simply choosing the color combination you want :
<a href="https://getmdl.io/styles/index.html" target="_blank">Material Design Lite Styles</a>

</div>

<h3 class="fancy">Conclusion:</h3>

I loved working with Material Design Lite, it is a very simple and to the point CSS framework, I guess the main question is how does it stack against something like Bootstrap and the other Material Design Frameworks. In my brief experience, it is not as complete and customizable as bootstrap, or App friendly as something like Angular Material, yet if you want to add The material design look to a simple site it is a great option, additionally if you want to use the Google sanctioned implementation this is the only one.

I hope you enjoyed this few code samples and overview of Material Design Lite.

Best,

Keno
