---
layout: post
title: 'Everyday Javascript: Objects.'
excerpt: A new series on everyday Javascript issues and coding techniques, let's start by looking at Objects and some ways of using them.
permalink: /everyday-javascript-objects
smlogo: Js.png
---
<div class="text-center"><img src="assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Welcome</h3>

This is a new series on common Javascript problems, techniques and solutions I've encountered, in this first post, I'd like to talk a bit about Objects in Javascript, come along and learn by example.

<h3 class="subHeader">Why Objects ?</h3>

Good question, you can write a program without ever making an object, in my mind, objects make sense when you want to make a bunch of things and want each of them to be a <i>precious and unique snowflake</i>.

<div class="note"><b>Note: </b> I will be using <a href="http://jdan.github.io/isomer/" target="_blank"><b>Isomer.js</b></a> ( a cool tinsy isometric graphics library to render cubes) along with <a href="http://www.createjs.com/easeljs" target="_blank"><b>easel.js</b></a> (a canvas management library used for hit detection) and some <a href="http://getbootstrap.com" target="_blank"><b>bootstrap</b></a> ( to center and align content) these are entirely optional for learning about objects, if you need an introduction to Isomer, here's a related post:
[Isometric Graphics with Javascript]({{ site.baseurl }}//isomerJS){:target="_blank"}
</div>

Let's first look at the following example where objects are <b>NOT</b> being used: 2 Isometric cubes are created, hit detection bitmaps created and mouseEvents attached, check it out:

<p data-height="600" data-theme-id="27284" data-slug-hash="VmJjvG" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Isomer MouseOver Click Example" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VmJjvG/">Isomer MouseOver Click Example</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Just to reiterate, there is nothing wrong with this approach, and sometimes it is simpler and clearer to not use objects,especially as you are figuring out things,the main issue is that this example is not easily scalable as written and quickly becomes a nightmare to write and maintain if we increase the number of cubes from 2 to say 10, don't believe me, you try it:

<div class="challenge"><b>I Challenge you:</b> Without using Objects increase the number of cubes from 2 to 3 and then 10; <b>Hint:</b> I commented the lines <b>//</b> you would need to write and modify a 3rd time first, and then another 7 times for around 112 extra lines of code.</div>


<h3 class="subHeader">Enter Objects</h3>

Like many things in programming, there are more than one way of doing things, so, Objects can be defined and created in a couple of ways, here are 3 common ways to do it.

<p data-height="600" data-theme-id="27284" data-slug-hash="bgrqzz" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Isomer Objects" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/bgrqzz/">Isomer Objects</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="challenge"><b>Fun Fact</b> If you want to increase the number of cubes in any layer, you now only need to modify one variable and write no extra lines, you could also increase the cubes size, color etc, try it, the relevant lines are commented <b>//</b></div>


<div class="note"><b>Note: </b> ES6 the new and shinny version of Javascript brings yet another way you can create objects with the class syntax, here is an in depth comparison and introduction to classes in Javascript if you want to explore them :
[ES6 Sampler #3: (Classes)]({{ site.baseurl }}/es6-classes){:target="_blank"}
</div>

<h3 class="subHeader">Object Methods</h3>

So now that we have explored how to create a bunch of objects, it is time to start working with them,wrangle them into submission if you will; a very common thing you might want to do, is modify every single object at the same time, in order to do this, you simply create a method in your object definition and call it for each instance, let's look at an example:

<div class="note"><b>Note: </b> So out of the 3 (4 if you count classes) ways of creating objects, which one is the best ? I personally like object literals with in line methods, but, and this is a big butt, every method will be recreated along with the object, which arguably translates into less performance. I settled then (at least for the rest of the examples here), with a hybrid Constructor definition plus outside prototype methods to be on the safe side.
</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="YNxQmW" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Isomer Object Methods" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YNxQmW/">Isomer Object Methods</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="challenge"><b>Try it: </b> So to continue expounding on why objects make things easier, there are 2 object methods in this example, one renders the cube, and the other animates it, so if you wanted to affect all your cubes, you would only need to change one update function and all the cubes would follow your orders, you can try this by modifying the commented lines <b>//</b>
</div>

<h3 class="subHeader">Naming your Snowflakes</h3>

The next step towards object domination is figuring out a way to make each object a truly unique thing, in the next sample, we will name each one of the objects and later identify them so we can change them on a one by one basis.

<div class="note"><b>Important Note: </b> In order to keep track of our objects, we will need to create what is normally called a <b>Dictionary</b>, a place where we will keep references to other objects, while using an array is also possible at times, a dictionary allows you to store key value pairs ( in our case object name and object), the interesting and perhaps confusing thing, is that the syntax for the dictionary is the same as that of an object literal: <code> <b>var preciousSnowflakes = {}; </b></code>, or more profoundly,objects are dictionaries of key/value pairs whose properties and methods can be added,removed and modified at runtime.
</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="BpmRXe" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Isomer Object properties" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/BpmRXe/">Isomer Object properties</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="challenge"><b>Power Tip:</b> You can inspect your Dictionary and recently created objects in your console, just log them : <br />
<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/ObjectConsole.jpg" alt="Object Console">
</div>

<h3 class="subHeader">Animating your objects</h3>

Another thing you might want to do with your objects,<i>an example of a complex behavior </i>is subscribe them to a render loop so you can animate them on an individual basis, the following example shows just how to do that by modifying the existing object definition and extending the draw method from the previous examples.

<div class="note"><b>Note: </b> As mentioned, there are a few ways to work with objects, to keep things simple, I am not using getters and setters, which allow you to return complex/computed  properties after being calculated in a function within the object, so in theory you can also animate by using them, you can read more about them and other object features here: <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#Defining_getters_and_setters" target="_blank"><b>Working with Objects, Defining getters and setters</b></a>

</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="NdwooV" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Isomer Object Render Loop" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NdwooV/">Isomer Object Render Loop</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="challenge"><b>Adding more complexity </b> Using this strategy you can easily add complex and individualized behavior to your objects, you can try it by simply adding new behavior to the draw method.</div>

<h3 class="fancy">Last words...</h3>

I still think that the easiest way to deal with objects as you are programming is to ask yourself, am I creating a lot of individual snowflakes ? , if the answer is yes, learning how to deploy, keep track and modify them will surely make your life easier and your Javascript coding more fun and effective.

Best,

Keno
