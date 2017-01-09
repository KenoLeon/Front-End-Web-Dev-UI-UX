---
layout: post
title: 'Getting to know Typescript Part 1.'
excerpt: Typescript is a curated superset of Javascript that adds a lot of extras, it's also very popular, so come and check it out.
permalink: /TypescriptPt1
smlogo: TS.png
---
![javascript](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/TSLogo.jpg)

<h3 class="fancy">Preface</h3>

I normally like my Javascript like my ice cream: plain and Vanilla, but that doesn't mean I am not open to new flavors, <a href="https://www.typescriptlang.org/" target="_blank"><b>TypeScript</b></a> seems to be one of those new Javascript flavors, "<i>Javascript that scales</i>" as they promise. So come along and follow me as I try to figure out this new thing.

<div class="step"> <b>Step 1: </b> Set up TypeScript </div>

On a first quick pass, TypeScript introduces <a href="https://www.typescriptlang.org/docs/tutorial.html" target="_blank"><b>Type Annotations</b></a>, handy definitions for variables:

<code> function(**arg: string**){
    //use string argument }</code>  

 The above bit of code should throw a warning when not receiving a string as an argument.


 The first gotcha, is the following example:

 <p data-height="396" data-theme-id="0" data-slug-hash="pRoveN" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript 001" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/pRoveN/">TypeScript 001</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

TypeScript is a superset of Javascript, which means that whatever runs in Typescript will probably also run in Javascript, in order to see a warning about an incorrect type, we would need a different setup so...

<div class="step"> <b>Step 1b: </b> Set up TypeScript on an IDE/text editor/desktop environment</div>


- I am going with <a href="https://atom.io/" target="_blank"><b>Atom</b></a> (Cause it's free and awesome).

- Start by installing <a href="https://atom.io/packages/atom-typescript" target="_blank"><b>Atom-Typescript</b></a>

<div class = "note"><b>Note:</b> You will probably also need a tsconfig file :  <a href="http://stackoverflow.com/questions/32233148/atom-typescript-complaining-about-tsconfig-json-how-can-i-automatically-create" target="_blank"><b>cmd(ctrl)+shift+p + tsconfig</b></a></div>

  You will now be able to make <b>.ts - Typescript</b> files and Atom will warn you when your types are wrong:

![Atom-TypeScript warning](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomTypeScript.jpg)

<h3 class="fancy">Variable Types in Typescript</h3>

<div class="step"> <b>Step 2: </b> What are some basic types in Typescript ? </div>

<div class = "challenge"><b>Note:</b> Typescript prefers the use of the more modern <b>LET</b> when declaring variables.</div>

<p data-height="900" data-theme-id="0" data-slug-hash="jyOKEw" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Types" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/jyOKEw/">TypeScript - Types</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<div class = "note"><b>The more you know</b> If you are like me, you might be thinking why learn all these new stuff, what makes Typescript scale etc,etc, in as few words as possible, Javascript is dynamically typed and as such variables are instantiated at run-time, Typescript is Static, so there are no surprises and less bugs, for a full discussion check this: <a href="http://stackoverflow.com/questions/12694530/what-is-typescript-and-why-would-i-use-it-in-place-of-javascript" target="_blank"><b>What is TypeScript and why would I use it in place of JavaScript?</b></a> </div>

<h3 class="fancy">Interfaces</h3>

Typescript also brings Interfaces to Javascript (see Note)so...


<div class="step"> <b>Step 3: </b> Make an interface, figure out what an interface does</div>

<div class = "note"><b>The more you know</b> So what's an interface and what is it good for you ask. In general, an interface is a description of the actions that an object can do or the properties it should have, in other words this class/object  must have these functions/things and it is valuable because well it prevents you from designing some object or class and later misconfiguring it</div>

<p data-height="500" data-theme-id="0" data-slug-hash="YNPMye" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Interfaces" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YNPMye/">TypeScript - Interfaces</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

So we have a basic interface and a function that implements it, to see it fail and why it is useful, we need to go back to our desktop editor and try to compile our typescript file, you will get the following error if you ommit part of the interface:

![Atom-TypeScript interface error](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomInterfaceError.jpg)

<h3 class="fancy">Classes</h3>

Besides Interfaces and Types, Typescript adds Classes to Javascript, which you might already be using if you do ES6 ( See note ) and code sample.

<div class = "note"><b>The more you know</b>Javascript normally dealt with object based inheritance via the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain" target="_blank"><b>protoype syntax</b></a>, in es6 ( new and shinny Javascript), the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes" target="_blank"><b>class syntax</b></a> was introduced, which in turn is just a new name or syntactic sugar for protoypes. Typescript allows for the use of classes even when there is no browser support ( like babel or a polyfill does) plus it also adds some other niceties</div>

<div class="step"> <b>Step 4: </b> Make a class in Typescrypt</div>

<p data-height="760" data-theme-id="0" data-slug-hash="RKNoNX" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Classes" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/RKNoNX/">TypeScript - Classes</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

And breaking our new class is just a matter of ommiting a variable..

![Atom-Typescript Class error](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomClassError.jpg)

<div class = "challenge"><b>Note:</b>In order to convert Javascript to Typescript, your editor will help you by pointing out the missing bits like so:
</div>

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomJavascriptToTypescript.jpg" alt="Atom-Typescript">


<div class="step"> <b>Step 5: </b>Class inheritance & other Classy things </div>

Like in Javascript's es6, Typescript provides some extra handy features to the Class syntax, let's explore.

<b>Extending Classes</b>

<p data-height="1200" data-theme-id="0" data-slug-hash="qRdmRJ" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Class Inheritance" class="codepen">See the Pen <a href="https://codepen.io/k3no/pen/qRdmRJ/">TypeScript - Class Inheritance</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<b>Class Modifiers: Public & Private</b>

<div class = "note"><b>The more you know</b> What, why use them ?...Class Modifiers or Access Modifiers are very common on other languages like Java,C#, C++ etc, they  allow for control over who gets to access your object variables and methods, and using them is a good idea for security and convenience.</div>

<p data-height="700" data-theme-id="0" data-slug-hash="Ndqoqq" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Class Modifiers" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/Ndqoqq/">TypeScript - Class Modifiers</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

So while this example still compiles an runs, in your editor you would get errors:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomModifierError.jpg" alt="Atom-Typescript Modifier error">

<div class = "challenge"><b>Note:</b>There are more modifiers in Typescript beyond these basic two, <a href="https://www.typescriptlang.org/docs/handbook/classes.html" target="_blank"><b>check the Docs for the rest</b></a></div>

<h3 class="fancy">Conclusion:</h3>

There are quite a few other things that Typescript adds to Javascript, I'll try covering the rest on a second post, you can also check the full feature set from them, but for now I leave fairly impressed on how easy it is to get into Typescript.

Best,

Keno
