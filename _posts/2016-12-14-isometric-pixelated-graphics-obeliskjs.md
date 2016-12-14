---
layout: post
title: 'Obelisk.js Pixelated Isometric graphics with Javascript.'
excerpt: Obelisk.js is another great little Isometric graphics javascript library with a pixelated focus, come build something.
permalink: /obeliskJS
smlogo: ObeliskJS.jpg
---
<div class="text-center"><img src="assets/images/ObeliskJS.jpg" alt="obeliskjs"></div>

<h3 class="fancy">Preface</h3>

I was recently checking out a tiny Isometric javascript library called [Isomer.js]({{ site.baseurl }}/isomerJS){:target="_blank"}, and while researching I found out about <a href="https://github.com/nosir/obelisk.js/" target="_blank">Obelisk.js</a>, another Isometric Javascript library with a pixelated focus, let's figure out how to use it.  


<div class="step"> <b>Step 1: </b> Include Obelisk.js in a pen and display a cube</div>

<p data-height="600" data-theme-id="0" data-slug-hash="dOmQPE" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="obelisk step 1" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/dOmQPE/">obelisk step 1</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 2: </b> Make a grid and figure out Coordinates</div>

<p data-height="600" data-theme-id="0" data-slug-hash="WoJOOj" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 2." class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WoJOOj/">Obelisk.js Step 2.</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<div class="step"> <b>Step 3: </b> Make more grids !</div>

<p data-height="500" data-theme-id="0" data-slug-hash="BQVjpw" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 3." class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/BQVjpw/">Obelisk.js Step 3.</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 4: </b> Test out primitives</div>

<p data-height="600" data-theme-id="0" data-slug-hash="ZBRPgo" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 4. Primitives" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ZBRPgo/">Obelisk.js Step 4. Primitives</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 5: </b> Figure out colors: </div>

<p data-height="600" data-theme-id="0" data-slug-hash="KNBGjK" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 5. Colors" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KNBGjK/">Obelisk.js Step 5. Colors</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 6: </b> Animate a cube </div>

<div class="note">
<i><b>Caveat Emptor </b>( buyer beware )</i> Obelisk.js is not a full fledged Isometric or 3D tile engine, there are no shadows, lights,interactions, transforms,etc,etc. Look at three.js if you want more, although it is considerably larger in size and complexity, the alternative, is to use Canvas methods like on the following examples, but you will have to make them from scratch.
</div>

<p data-height="600" data-theme-id="0" data-slug-hash="KNxrmw" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 6 Animation" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KNxrmw/">Obelisk.js Step 6 Animation</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 7: </b> Explore Transforms </div>

<div class="note">
<i><b>More Caveat</b></i> Simple translations ( moving the cubes) and even scaling are fairly simple, I chickened out when it came to rotations, why ?, well in order to rotate the cube or any other primitive we would need to rotate the coordinate system,modify the light source,color buildup and a couple of other things, in other words we would need to extend considerably the library, and this is but a humble introduction... bwok bwok!

</div>

<p data-height="600" data-theme-id="0" data-slug-hash="XNPGGa" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 7. Transforms" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/XNPGGa/">Obelisk.js Step 7. Transforms</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="step"> <b>Step 8: </b> Make something pretty </div>

<p data-height="600" data-theme-id="0" data-slug-hash="pNOBBL" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Obelisk.js Step 8. Pretty Chicken" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/pNOBBL/">Obelisk.js Step 8. Pretty Chicken</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<i>Chickens are kinda pretty I suppose :)</i>

<h3 class="fancy">Parting words</h3>

Obelisk.js is a really cool little library for cranking out pixelated graphics, I kept thinking this library along with the recently reviewd Isomer.js could be used for some basic games, unfortunately, there is still a lot of code to build for them to compete with something like three.js, but the oportunity is there, on the other side if all you want is some cool graphics, are looking to a project to contribute to either one will do, they are both awesome.

Best,

Keno.
