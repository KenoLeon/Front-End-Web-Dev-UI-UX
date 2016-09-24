---
layout: post
title: Let's try Angular Material.
excerpt: Angular Material is a cool Front End Library using Material design for the Angular framework,let's check the basics...
permalink: /lets-try-Angular-Material
smlogo: Angular.png
---



![Angular Material]{{ site.url }}(assets/images/AngularMaterial.jpg){:class="img-responsive"}


<h3>Preface:</h3>

As part of my series on learning Angular, I am checking out [Angular Material](https://material.angularjs.org/latest/){:target="_blank"}, a cool library for implementing [Googles Material Design](https://material.google.com){:target="_blank"} with Angular, come along and check it out !

<i class='Note'>Note : this is some intermediate Angular stuff, check out my previous posts if you are just getting started:<i/>

- [Getting started with Angular JS](http://codepen.io/k3no/post/getting-started-with-angularjs){:target="_blank"}
- [More Angular JS Pens](http://codepen.io/k3no/post/more-angular-js-pens){:target="_blank"}

<i class='Note'> Also Note : Change is coming... Angular 2 is just around the corner, but for the time being we'll be working with Angular and Angular Material 1 since they are well documented/stable <i/>

<div class="challenge"> <b>Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3>Pre flight Check:</h3>

- [Angular Material Website](https://material.angularjs.org/latest/){:target="_blank"} - Check The release though, this post was made with 1.1.1  
- [Google Material Design](https://material.google.com){:target="_blank"} - Read it (long read) or gloss over the documentation to get acquainted with the style,what,why,etc. In production you will most likely be given a wire frame from a designer, but if you are a one man show, it's up to you to keep things consistent or not.

<h3>Ok, Let's get started </h3>

<div class="challenge"><b>Challenge: </b> Import Angular material and display a component, any component.</div>


<p data-height="605" data-theme-id="0" data-slug-hash="XjmGWQ" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/XjmGWQ/">Angular Material Hello World</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


And there you have it sir, the very simple but ubiquitous cat card component, what did we learn ? couple of things:

- 1. You need to import a few scripts plus the CSS ( Check the settings )
- 2. It works like a charm and a lot like Bootstrap ( Check the HTML )

**In General :**

- Start with the directive, in this case [md-card](https://material.angularjs.org/latest/api/directive/mdCard){:target="_blank"}
- And if you get stuck check their demos:[Card Demo](https://material.angularjs.org/latest/demo/card){:target="_blank"}

<h3>Grids</h3>

Layouts are a huge part of what makes a front end library useful, let's look at what Angular Materials has to offer.

<div class="challenge"><b>Challenge: </b> Use the grids provided by angular and create a responsive layout.</div>

<p data-height="265" data-theme-id="0" data-slug-hash="bwEwGz" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/bwEwGz/">Angular Material Layout</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b>Lessons learned ?</b>  Angular Material builds on top of flexbox via directives to specify your layout, sounds a little complicated, but in reality ( after a bit of trial and error), it goes like this:

- 1. Add a Layout directive and specify a row or Column flow, add responsive layouts attributes
- 2. Add content

Like any other grid system ( think Bootstrap) there are specific breakpoints for different devices and a host of other niceties to center, add padding, hide, order etc,etc, a good way to get into them is checking the very nice documentation:

- [Layout Introduction](https://material.angularjs.org/latest/layout/introduction){:target="_blank"}


Since Layouts are such a big part of development, let's dig deeper.

<div class="challenge"><b>Challenge: </b> Create a layout with extra options; for example a 3 column padded responsive layout with hidden content that is centered, yowzaa! </div>

<p data-height="324" data-theme-id="0" data-slug-hash="WGAGav" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WGAGav/">Angular Material Complex Layout</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

So like bootstrap, you concatenate or chain options to both the layout container and the individual content blocks to affect display ( following flexbox conventions ), only here you do it with directives instead of classes, all the [extra options](https://material.angularjs.org/latest/layout/options){:target="_blank"},[troubleshooting](https://material.angularjs.org/latest/layout/tips){:target="_blank"} and [details](https://material.angularjs.org/latest/layout/alignment){:target="_blank"} are explained in the very concise documentation.

<h3>More Complex Directives</h3>

Now that we have a decent grasp of the basics ( or so I hope), let's explore more interactive elements, let's start with an autocomplete:

<div class="challenge"><b>Challenge: </b>Use Angular Material's  autocomplete directive </div>

<p data-height="265" data-theme-id="0" data-slug-hash="NRxOVg" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NRxOVg/">Angular Material Autocomplete</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

A super minimal example of autocomplete, note I am also using googles material icon library, in a nutshell, the autocomplete provides handles for expressions in the model and options (extra directives) for customizing your autocomplete, if you get stuck or want to implement a real world autocomplete, consult the docs...

- Directive Documentation: [md-autocomplete](https://material.angularjs.org/latest/api/directive/mdAutocomplete){:target="_blank"}
- Demos: [AutoComplete  Demos](https://material.angularjs.org/latest/demo/autocomplete){:target="_blank"}

<h3>Multiple Directives</h3>

Feeling a little more confident, so let's try adding more than one  directive inside a layout to up the ante.

<div class="challenge"><b>Challenge: </b>Use multiple directives inside a layout, make it awesome.</div>

<p data-height="700" data-theme-id="0" data-slug-hash="vXLPAx" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vXLPAx/">Angular Material Multiple Directives + Layout</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And there you have it, a very,very,very simple semi functional ( I left out the model), but practical Angular Material App.

Directives Used:

- [md-whiteframe](https://material.angularjs.org/latest/api/directive/mdWhiteframe){:target="_blank"}
- [md-content](https://material.angularjs.org/latest/api/directive/mdContent){:target="_blank"}
- [md-datepicker](https://material.angularjs.org/latest/api/directive/mdDatepicker){:target="_blank"}
- [md-placeholder](https://material.angularjs.org/latest/api/directive/mdPlaceholder){:target="_blank"}
- [md-switch](https://material.angularjs.org/latest/api/directive/mdSwitch){:target="_blank"}
- [md-list](https://material.angularjs.org/latest/api/directive/mdList){:target="_blank"}
- [md-divider](https://material.angularjs.org/latest/api/directive/mdDivider){:target="_blank"}
- [ng-if](https://docs.angularjs.org/api/ng/directive/ngIf){:target="_blank"}

<h3>The Takeway</h3>

Angular Material is a powerful,complex and extensive companion to the Angular Framework, I tried my best to cover all the bases, but I left a lot of things out which hopefully I'll cover in a second post, I hope this serves you as a gentle introduction to Angular Material.


Best,

Keno
