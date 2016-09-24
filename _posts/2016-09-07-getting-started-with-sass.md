---
layout: post
title: A gentle introduction to Sass
excerpt: Come explore what Sass - a popular Css preprocessor -  can do for your Css with a gentle introduction and code samples.
permalink: /gentle-Sass
smlogo: Sass.png
---



![Sass]{{ site.url }}(assets/images/sassLogo.png){:class="img-responsive"}


<h3>Preface:</h3>

Sass is a great little helper for dealing with complex CSS and extending functionality, come along and learn about [SASS](http://sass-lang.com){:target="_blank"}.

<i>Note: I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</i>


**Sass Syntax(es)**

> Challenge: Import and display some html styled in Sass Syntax ( Both of them ! )


The first thing I feel I need to clarify, is that there are 2 (Two) different ways to write SASS, let's check out both with a simple example, this example will also show how to nest  Css selectors,( a Sass feature), let's start with the result:


<p data-height="320" data-theme-id="0" data-slug-hash="mAydNk" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/mAydNk/">Sass Syntax Overview ( Plain CSS )</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>



<p data-height="280" data-theme-id="0" data-slug-hash="ORPJdL" data-default-tab="css" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ORPJdL/">Sass Syntax Overview ( SCSS )</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<p data-height="280" data-theme-id="0" data-slug-hash="ALjBGQ" data-default-tab="css" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ALjBGQ/">Sass Syntax Overview ( Sass )</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

**The main differences in between syntax styles:**

- Lack of semicolons and brackets on (Sass) Syntax
- Semicolons and Brackets on (Scss) Syntax

**Nesting**

- You nest by Indenting the selector/element in (Sass) Syntax
- You nest with Brackets in (Scss) Syntax

[There is a nice write up on the documentation about why and what the differences are...](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax){:target="_blank"}

As for which one to use, [it is up for debate](http://thesassway.com/editorial/sass-vs-scss-which-syntax-is-better){:target="_blank"}, currently( Mid-Late 2016), I believe Scss is slightly more popular with the crowd and Sass is [more of a niche](https://www.reddit.com/r/Sass/comments/3iddes/scss_vs_sass/?){:target="_blank"}, so in the interest of setting you ( dear reader) for success, I'll use only SCSS going forward

**Variables:**

One of the biggest things you can do with Sass, is define and use variables, let's check how:

>Challenge: Define and use at least 2 Sass variables.

<p data-height="500" data-theme-id="0" data-slug-hash="VKYmvZ" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VKYmvZ/">Sass Variables</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

As you can see, you declare and use variables with the dollar sign **$** , this is super handy when you have complex sites with tons of elements and you want to change some related colors for instance.

**Data Types:**

This is just the tip of the iceberg,  you can use various [ Data Types](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#variables_){:target="_blank"} and [operations](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations){:target="_blank"}, let's check out the different data types you can use with sass first:

> Challenge: create 2 variables that use different data types and use them

<p data-height="499" data-theme-id="0" data-slug-hash="xEbRXG" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xEbRXG/">Sass Data Types</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And the rest ([from the docs](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#sass-script-strings){:target="_blank"}) :

- <i>numbers (e.g. 1.2, 13, 10px)</i>
- <i>strings of text, with and without quotes (e.g. "foo", 'bar', baz)</i>
- <i>colors (e.g. blue, #04a3f9, rgba(255, 0, 0, 0.5))</i>
- <i>booleans (e.g. true, false)</i>
- <i>nulls (e.g. null)</i>
- <i>lists of values, separated by spaces or commas (e.g. 1.5em 1em 0 2em, Helvetica, Arial, sans-serif)</i>
- <i>maps from one value to another (e.g. (key1: value1, key2: value2))</i>

**Operations:**

So far so good,things start getting more complex and useful once you consider that Sass add the ability [to do operations within Css,](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations){:target="_blank"} let's start with some basic ones:

> Challenge: Use some Basic operations in Sass

<p data-height="488" data-theme-id="0" data-slug-hash="LREmbX" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/LREmbX/">Sass Basic Operations</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

**Conditionals**

A slightly more complex (but awesome ) use of operations in Sass is with conditionals:

> Challenge: Create a conditional in Css with Sass !

<p data-height="616" data-theme-id="0" data-slug-hash="VKYxzO" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VKYxzO/">Sass Conditionals</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

This being an introduction, I'll leave with a simple conditional, but there is more, you can use [@if, @for, @each and @while control structures as well !](http://thesassway.com/intermediate/if-for-each-while){:target="_blank"}

**Functions**

Another cool feature of Sass is the [included functions](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#functions){:target="_blank"}


>Challenge: Use a Sass function, any function.


<p data-height="497" data-theme-id="0" data-slug-hash="ozgdqO" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ozgdqO/">Sass Functions</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

[Full list of built-in-functions](http://sass-lang.com/documentation/Sass/Script/Functions.html){:target="_blank"}

And for an advanced related topic, you can also [create your own Sass functions](http://thesassway.com/advanced/pure-sass-functions){:target="_blank"}

**Imports**

As their name implies, imports allow you to add another chunk or segment of CSS ( CSS already allows imports, but Sass generates a single file, so you can save on requests).

> Challenge: Import some Css into a Sass file.

<p data-height="265" data-theme-id="0" data-slug-hash="gwbNvQ" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/gwbNvQ/">Sass Imports</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Note: the above is just an example using plain Css Imports ( due to how codepen works), in a local environment you would us something like:

<pre>@import 'defaultStyle'; </pre>

Check the rest of the [Sass Import documentation for more.](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#import){:target="_blank"}


**Mixins**

And last but not least,let's take a look at mixins,  what's a mixin you ask ? good question....

> Challenge: Figure out what a mixin is and make and use one.

<p data-height="454" data-theme-id="0" data-slug-hash="ALvjKo" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ALvjKo/">Sass Mixins</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

A mixin is a just a collection of css declarations you can then later reuse, you can make mixins for vendor prefixes, small and large components and other useful bits of css, you define them with **@mixin** and use them with **@include** but there's more, you can also add arguments and thus make them into function ! let's try that:

> Challenge: Create a mixin with arguments and use it.

<p data-height="564" data-theme-id="0" data-slug-hash="PGqwmo" data-default-tab="css,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/PGqwmo/">Sass Mixins with Arguments</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And that's that, you can check the documentation for more about [making your own mixins with arguments](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#defining_a_mixin){:target="_blank"}

>Things I didn’t cover/further challenges: Other directives like @function and control directives, extending Sass, lists and maps and complex mixins, plus the sass ecosystem.

**The Takeaway:**

Sass does give css super powers as they say, it takes a little getting used to the syntax and wrapping your head around the new css functionality, but if you learn it you will become more productive, it is also worth mentioning that some of the Sass functionality is being slowly incorporated into css, but it's still worth to learn sass since there is a healthy ecosystem of libraries that build on top of sass to make Front End development better and faster.

Best,

Keno
