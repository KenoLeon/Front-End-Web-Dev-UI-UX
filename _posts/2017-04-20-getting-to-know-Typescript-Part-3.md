---
layout: post
title: 'Getting to know Typescript Part 3.'
excerpt: A third and final overview at what Typescript brings to Javascript and why you should or shouldn't consider using it,come along !
permalink: /TypescriptPt3
smlogo: TS.png
---
![javascript](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/TSLogo.jpg)

<h3 class="fancy">Preface</h3>

Somehow overdue cause I moved countries, here is the final look at Typescript, let's check out some of the other things that Typescript has to offer.

<div class="speechBubble">Check out the other posts on this series,a good place to start if like me you are getting started with Typescript:
</div>

- [Getting to know Typescript Part 1.]({{ site.baseurl }}/TypescriptPt1){:target="_blank"}
- [Getting to know Typescript Part 2.]({{ site.baseurl }}/TypescriptPt2){:target="_blank"}

<h3 class="fancy">Modules</h3>

Modules seem to be a way to organize your typescript code better, let's see what they entail...

<div class="step"> <b>Step 1: </b>Make and use a module</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="dWPOpj" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Modules" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/dWPOpj/">TypeScript - Modules</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

I'll be honest, modules seem to be a bit difficult to grasp at first and might be a deeper subject not suitable for an introduction, for now, let's just cover the basics. The above is a simple internal module; why would you want to use an internal module ? well you can encapsulate behavior, variables, methods etc; notice for instance that the second class function is not getting out.

This was a handy internal module to showcase basic module behavior, but more likely you will encounter modules in multiple external files, let's split the above sample into 3 files:

<div class="step"> <b>Step 2: </b>Make and use <b>external</b> modules</div>

The first file will be ***Module1.ts***:

```typescript
export function saySomething() {
       console.log('I am a function inside module 1');
    }   
```

And a second file ***Module2.ts***:

```typescript
export class m1Class {
  // add other class stuff here
  sayMore() {
    console.log('I am a class method inside module 2');
  }
}
```

And finally a loader file (***Loader.ts***):

```typescript

import * as module1 from "./Module_1";
module1.saySomething();

//I am a function inside module 1

import { m1Class } from  "./Module_2";
var classy = new m1Class;
classy.sayMore();

// I am a class method inside module 2

```

Notice that now the file names are used as the module names, that you can import the whole module or just parts of it. Modules are tricky because on top of this basic functionality there is a lot of nuance and functionality, you can explore more on the docs:  

<a href="https://www.typescriptlang.org/docs/handbook/modules.html" target="_blank"><b>Typescript Handbook: Modules</b></a>

<h3 class="fancy">JSX Support</h3>

<a href="https://facebook.github.io/react/docs/introducing-jsx.html" target="_blank"><b>JSX:</b></a> The unholly marraige of HTML & Javascript was introduced along with React by facebook, typescript is jumping on this, let's try writing some JSX in Typescript:

<div class="step"><b>Step 3</b>: Write some JSX in Typescript </div>

<div class ="note"><b>Note: </b> You need to import React and know a bit about it for this to make sense, I did a few introductory tutorials you might want to check: <a href="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/Getting-Started-With-ReactJs" target="_blank"><b>Getting Started With React</b></a></div>



<p data-height="400" data-theme-id="27284" data-slug-hash="xdGVjp" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - JSX" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xdGVjp/">TypeScript - JSX</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

There's not much to it, but what if we want to typeCheck JSX? (*else why use typescript*)...

<div class="step"><b>Step 3.b</b>: Write & Type Check some JSX in Typescript ! </div>

<p data-height="400" data-theme-id="27284" data-slug-hash="xdGXjP" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - JSX -Types" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xdGXjP/">TypeScript - JSX -Types</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Again not much to it, ( but still awesome ), you can use typechecking/typescript along with react,neat.

There is of course more to it: <a href="https://www.typescriptlang.org/docs/handbook/jsx.html" target="_blank"><b>Typescript Handbook: JSX</b></a>


<h3 class="fancy">Mixins</h3>

A mixin is usually a snippet of code or css you can reuse, a functions cousin if you will, Typescript supports mixins, let's check them out:

<div class="step"><b>Step 4</b>: Create and use a mixin.</div>


<p data-height="1200" data-theme-id="27284" data-slug-hash="NjGEXN" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Mixins" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NjGEXN/">TypeScript - Mixins</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class ="note"><b>Note: </b> So when would you use a mixin ? according to the fine people at <a href="https://stackoverflow.com/questions/533631/what-is-a-mixin-and-why-are-they-useful?rq=1" target="_blank"><b>Stack Overflow</b></a>: <br /><br />

A mixin is a special kind of multiple inheritance. There are two main situations where mixins are used:<br />

<ul>
<li> You want to provide a lot of optional features for a class. </li>
<li> You want to use one particular feature in a lot of different classes. </li>
</ul>

Sounds good to me.
</div>

So mixins are a mixed bag, you can probably get the same functionality from plain functions and classes, but if you can overlook the syntax and helper functions needed and you like the way they work/look, go for it. More about mixins in Typescript:   <a href="https://www.typescriptlang.org/docs/handbook/mixins.html" target="_blank"><b>Typescript Handbook: MIXINS</b></a>

<h3 class="fancy">Namespaces</h3>

So we have covered a lot of what Typescript has to offer, but there is still more, although this is still a beginners guide, an overview of a few more advanced topics I think is needed, let's start with namespaces:

<div class ="note"><b>Note: </b> So What is a namespace anyways ?<br />
<a href="http://stackoverflow.com/questions/991036/what-is-a-namespace" target="_blank"><b>From stackOverflow</b></a> "A namespace provides a container to hold things like functions, classes and constants as a way to group them together logically and to help avoid conflicts with functions and classes with the same name that have been written by someone else."
</div>


Let's try writing some namespaces in Typescript...

<div class="step"><b>Step 5</b>: Create namespaces in Typescript.</div>

<p data-height="700" data-theme-id="27284" data-slug-hash="mmVXqp" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Namespaces" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/mmVXqp/">TypeScript - Namespaces</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

So namespaces provide a nice way of keeping things in order and avoiding conflicts, more complex scenarios can be found in the Docs: <a href="https://www.typescriptlang.org/docs/handbook/namespaces.html" target="_blank"><b>Typescript Handbook: Namespaces</b></a>

<div class ="note"><b>Note: </b>Namespaces in Typescript can be a deep dive, when using external Javascript libraries for instance, you might want to add a <a href="https://www.typescriptlang.org/docs/handbook/declaration-files/introduction.html" target="_blank"><b>declaration file</b></a> ( there's a repo of them here: <a href="https://github.com/DefinitelyTyped/DefinitelyTyped" target="_blank"><b>Github:DefinitelyTyped</b></a>).  
</div>

<h3 class="fancy">Conclusion:</h3>

While Typescript might or might not be your first choice when coding something in Javascript, it's sheer popularity ( and type checking ) makes it worth adding to your coding skills (especially if you are into Javascript), I hope this overview helps you !

Best,

Keno


<div class ="note"><b>Final Note: </b> You might still be wondering When to use Typescript ?<br /> We covered some reasons in the first part, but this little article goes further in depth (hint: Angular 2, performance , project size , etc) : <a href="https://medium.freecodecamp.com/when-should-i-use-typescript-311cb5fe801b" target="_blank"><b>When should I use Typescript ?</b></a>
</div>
