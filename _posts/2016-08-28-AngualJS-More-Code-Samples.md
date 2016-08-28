---
layout: post
title: More AngularJS introductory code samples .
excerpt: This is the second in an introductory series of AngularJS code samples, jump in !
permalink: /more-angularJS-code-samples
---


# **Preface...**

This is an ongoing series on Angular.js where you can learn by following a series of code samples and my own learning curve, before each one I gave myself a little challenge which you can use to learn on your own, so come along

Check the first part if you haven't already:

[Getting started with AngularJS]({{ site.baseurl }}/getting-started-with-AngularJs)

*Note: Change is coming... Angular 2 is just around the corner, but working with the current stable version of Angular 1 and then learning Angular 2 seems to be the correct path.

<h2>Routing</h2>

Ok, let's start with Routing in Angular.

> Challenge: Import angular-Route and make a navigation bar with routes to different pages with different content.

<p data-height="300" data-theme-id="0" data-slug-hash="zBQpAG" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/zBQpAG/">Angular Routes</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Routing in Angular has a few moving parts:


* Importing an external library.
* Configuring routing through $routeProvider.
* Displaying  content ( templates ) through ng-view.

If this sounds confusing,look at the code example for a minimal route, let us now look into how routes tie in with controllers and scope.

> Challenge: Route navigation to different controllers with different scope.

<p data-height="300" data-theme-id="0" data-slug-hash="Lkoqrr" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/Lkoqrr/">Angular Routes With Controllers</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

To bind a route to a controller just define it in and assign it in the $routeProvider, notice that each controller has it's own scope and methods (functions).

Another common thing with routing, is allowing the page to know its location, so let's figure that:

> Challenge: Add active indicators to the navigation bar with multiple routes.


<p data-height="300" data-theme-id="0" data-slug-hash="NAVVpP" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NAVVpP/">Angular Routes Active Links</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

This one took a little longer and involved exposing the Routes object to the navigation controller, it seems somehow complex,If you are doing a lot f routing, you might want to check [AngularUI](https://github.com/angular-ui){:target="_blank"} an angular routing framework that makes active links simpler.

<h2>Data</h2>

Enough about routes, lets look at fetching data:


> Challenge: Fetch some JSON data with angular

<p data-height="300" data-theme-id="0" data-slug-hash="YWopmb" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YWopmb/">Angular AJAX Http</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

This one was pretty simple and a great example of where angular shines, data is fetched or sent with the http service that angular includes as part of the core library, while the example is minimal, most of the communication with the server or external data can be made through the [$http service](https://docs.angularjs.org/api/ng/service/$http){:target="_blank"}, neat.

<h2>Modules</h2>

Before looking into directives, let's revisit modules in Angular:

> Challenge: Create a nested module structure.


<p data-height="300" data-theme-id="0" data-slug-hash="kXKyBL" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/kXKyBL/">Angular Modules</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Most of the action happens in the code (check the JS and HTMl); knowing how to nest and load modules seems handy for scalable applications, theres more about [modules on the docs](https://docs.angularjs.org/api/ng/function/angular.module){:target="_blank"} and even a [style guide](https://github.com/johnpapa/angular-styleguide){:target="_blank"}.

<h2>Directives</h2>

Besides Angular's own directives, you can also build your own, let's give that a shot.

> Challenge: Write a Custom Directive


<p data-height="300" data-theme-id="0" data-slug-hash="YWoJEO" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YWoJEO/">Angular Custom Directives</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

With custom directives Angular provides another way of encapsulating page elements, plus you get to create new tags with whatever name you want like:

    <apple-pie-directive></apple-pie-directive>


Another useful thing you can do with directives, is give them their own scope, let's try that:

> Challenge: Write a Custom Directive with it's own scope.

<p data-height="300" data-theme-id="0" data-slug-hash="OXZAbz" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/OXZAbz/">Angular Custom Directive Scope</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


As the complexity of your modules, templates ( partials in angular speak) and general application expands, communication and encapsulation of data through scopes becomes useful, there are more ways to deal with scope inside  directives and other details, just check the documentation for more

<h2>Form validation</h2>

For now, let's finish this second round of angular code samples by revisiting forms and how to validate them, check the first part if you need a refresher:

[Getting started with AngularJS]({{ site.baseurl }}/getting-started-with-AngularJs)


> Challenge: Create a form and validate an input with angular.

<p data-height="300" data-theme-id="0" data-slug-hash="PzAXvd" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/PzAXvd/">Angular Simple  Form Validation</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Validation happens automatically when adding the required value to the input alongside the ng-model and input field name, in this case we are still using bootstrap so the display validation is handled with a conditional, but Angular also provides a host of prebuilt [CSS  classes for validation](https://docs.angularjs.org/guide/forms){:target="_blank"}

Lastly, let's check more complex validations:

> Challenge: Create multiple input fields and validate them:

<p data-height="760" data-theme-id="0" data-slug-hash="NAQAwd" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NAQAwd/">Angular Multiple Inputs Validation</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

As you can see from theForm object dump, there is a lot more options; you can set validation values for many other form states and input types or send them over to a controller for further processing [( check the docs for custom validation )](https://docs.angularjs.org/guide/forms){:target="_blank"}.

And that's it for a second round of Angular code samples,I hope they help on your Angular learning voyage :)


Best, <br />
Keno
