---
layout: post
title: Introduction to Emmet
excerpt: Emmet is a real time saver when developing web pages, learn about it in this gentle Introduction
permalink: /introduction-to-emmet
smlogo: Emmet.png
---


## Quick explanation :

let's say you need to write down the following HTML code:

```html
<div class="row">
	<div class="col-md-6"></div>
	<div class="col-md-6"></div>
</div>
```


Using Emmet you would type the following:

```text
div.row>div.col-md-6*2
```

And then __dramatically__ press the  <kbd>TAB</kbd>  key on your keyboard, it will **expand** to the aforementioned html like magic.

<h3><b>Q: What do I need to use Emmet ?</b></h3>

- 1 : Almost nothing,online web editors like my favorite at the moment Codepen you already use it: [emmet in codepen](https://blog.codepen.io/2013/04/24/emmet-on-codepen/){:target="_blank"}. The html & css sections support Emmet,all you need to do is learn the syntax, but what about your local environment ?

- 2 : Depending on your Development Environment or Text Editor, you will have to download a plugin, here is a list of supported editors:
     [Emmet.io for your editor](http://emmet.io/download/){:target="_blank"}


<h3><b>A few basic Emmet commands to get you started:</b></h3>


- **Turn Html and non Html elements to Tags simply by typing the element plus :** <kbd>tab</kbd>

To get this:

```html
<div>
</div>
```

You would type this:

```text
div
```


- **Nest divs for your div soup with** <kbd>></kbd>

To get this:

```html
<div>
	<div>
		<div></div>
	</div>
</div>
```

You would type this:

```text
div>div>div
```


- **Add classes and Id's to your divs or elements with** <kbd>elem.</kbd> **and** <kbd>elem#</kbd>

To get this:

```html
<div class="classy1 classy2" id="peter"></div>
```

You would type this:

```text
div.classy1.classy2#peter
```

- **Add a sibling ( or parallel ) elements with**  <kbd>+</kbd>

To get this:

```html
<div></div>
<div></div>
<div></div>
```

You would type this:

```text
div+div+div
```

- **Multiply elements with**  <kbd>*</kbd>

To get this:

```html
<ul>
	<li></li>
	<li></li>
	<li></li>
	<li></li>
	<li></li>
</ul>
```

You would type this:

```text
ul>li*5
```

### Practice:

Here's a handy [pen](http://codepen.io/k3no/pen/QEkVJx){:target="_blank"} with a few more commands for you to practice your new found Emmet powers at your pace:

<p data-height="680" data-theme-id="0" data-slug-hash="QEkVJx" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="https://codepen.io/k3no/pen/QEkVJx/">Emmet Practice Dojo</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


### Further Reading:
<br />

 [Emmet Syntax](http://docs.emmet.io/abbreviations/syntax/){:target="_blank"}
 <br />
 [Cheat Sheet](http://docs.emmet.io/cheat-sheet/){:target="_blank"}

<br />
Hope you've enjoyed and learned a bit with this quick overview of Emmet.

Till next time.

Best,

Keno
