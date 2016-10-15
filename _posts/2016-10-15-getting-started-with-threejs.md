---
layout: post
title: '3D with Three.js '
excerpt: Three.js is the Current javascript library for 3D on the web, let's see how it works with some code samples...
permalink: /es6-classes
smlogo: threejssm.jpg
---

<div class="text-center"><img src="assets/images/threejsLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

Three.js seems to be the most popular 3D library at the moment (late 2016) , let's check out the state of 3d on the web with a few code samples.  

<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>


<div class="note"><b>Note:</b>3D is an advanced topic in programming,but mostly because there are a lot of terms and conventions, don't get discouraged if you feel a little lost at first, just look up the terms, additionally, some 2D animation experience and intermediate JS will help you.</div>


<h4 class="fancy">Let's 3D</h4>


<div class="challenge"><b>Challenge :</b>Import three.js and create a basic implementation</div>

<p data-height="600" data-theme-id="0" data-slug-hash="WGkkEx" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WGkkEx/">Three.js pt 1.</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


It might seem like a lot of code, but if you've ever worked with 3D, this is pretty normal, go through the code comments for a step by step of building a scene.   

So we have a scene and a rotating cube, where to go next ? well...

<b>Lights</b>
<div class="challenge"><b>Challenge :</b>Figure out how to create a light, illuminate a scene and cast a shadow in three.js</div>

<p data-height="600" data-theme-id="0" data-slug-hash="yapqLg" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/yapqLg/">Three.js pt 2.</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

It's not perfect, but it's a start, let's look at how to control a camera next so we can interact with the scene.

<b>Camera (Controls)</b>
<div class="challenge"><b>Challenge :</b>Figure out how to control a camera in three.js</div>

<p data-height="600" data-theme-id="0" data-slug-hash="WGrxOx" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WGrxOx/">Three.js pt. 3</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

As you might eventually find out, Three.js is loosely documented, or rather it is code documented, which means that in order to learn Three.js, you have to go through the examples and read the code, with the occasional visit to stackOverflow or other blog posts like this one.

I bring this up because in order to add camera controls, you need to figure out on your own that it is a) a different library some cool folks made, and b) it is documented in the comments, well now you know, but you see my point.

<b>Action</b>
<div class="challenge"><b>Challenge :</b>Figure out how to animate our cube</div>

<p data-height="600" data-theme-id="0" data-slug-hash="LRQrYo" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/LRQrYo/">Three.js pt. 4</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Look at it go!

There are of course more and more complex ways to animate things in Three.js, you can start by simply modifying the scene and geometry within your render loop,you can add a tweening engine, or import a physics library, I'll leave that to you or other future posts, for now, let's go back to basics and figuring out how to add custom materials to  our 3d cube.

<b>Materials</b>
<div class="challenge"><b>Challenge :</b>Figure out how to apply a material to a cube in three.js and what types of materials there are.</div>

<p data-height="600" data-theme-id="0" data-slug-hash="ZpAPRa" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ZpAPRa/">Three.js pt. 5</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

There are more types of materials and complexity, just check out the docs.

<b>Importing</b>
<div class="challenge"><b>Challenge :</b>Figure out how to import 3d models into three.js</div>

<p data-height="600" data-theme-id="0" data-slug-hash="ORvrJN" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ORvrJN/">Three.js pt.6 -Imports</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b>Interacting with the scene</b>

To round and complete this introduction to Three.js, let's learn how to interact with the objects in the 3D scene since that will probably come in handy.

<div class="challenge"><b>Challenge :</b>Figure out how to interact with our cube  or whale </div>

<p data-height="500" data-theme-id="0" data-slug-hash="WGzXGN" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WGzXGN/">Three.js pt.7 - Interact</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<div class="challenge"> <b>Further Challenges: </b> These are just some basic building blocks, next challenges would depend on what is it that you are trying to build, you  will also need to organize your code better, using objects with three.js and following a game pattern are good places to start, along with refinement of each of the above topics</div>

<h3 class="fancy">Conclusion:</h3>
Whoaa ! To be honest I had no idea if I was going to be able to finish a post on 3D basics with Three.js, it is a bit on the complicated side, but then again 3D is that kind of thing, I can now comfortably add some 3D to my projects and I hope these few code samples set you in the right 3D path.

<h3 class="fancy"> TL&#59;DR: </h3>

3D with Three.js Tough but rewarding.


Best,
<br />
Keno
