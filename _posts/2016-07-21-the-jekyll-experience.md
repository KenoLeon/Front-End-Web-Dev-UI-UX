---
layout: post
title: The Jekyll Experience
excerpt: My experience building a small blog ( this one) with a static site generator called Jekyll
permalink: /the-jekyll-experience
smlogo: jekyll.png
---

<h2><b>Preface</b></h2>

I've been building websites for more than a decade, you would think that by now I would have the absolutely best workflow for building a website, but alas, I am still learning and tweaking my workflow.

I recently wanted to build a simple blog for my site and wanted to avoid the bloat and maintenance of Wordpress,after consulting the oracles at Reddit, I went with [Jekyll](https://jekyllrb.com), a static website generator I haven't used before, here's my experience so far:


<h2><b>What,Why Jekyll ?</b></h2>

<img class="img-responsive" src="https://github.com/jekyll/brand/raw/master/jekyll-logo-black-red-transparent.png" alt="Jekyll Logo">

If you haven't used a static site generator, the big idea is that every time you make changes to your site files, your whole site gets rebuilt to reflect those changes, but unlike a CMS, you are mostly in charge of uploading your site to your server or host.

The biggest selling point is that you can include page and code variables and your file and folder structure works to make repetitive task easier, <span class="hl">things like pagination, code snippets, menu bars, post lists etc,etc become a breeze</span>; additionally, there is usually a template engine to help you import or make your own page templates.

<br />
<br />

There are so many out there, there is even a site that tracks them:

[Top Open-Source Static Site Generators](https://www.staticgen.com)

<br />
<br />
I gave Myself 1 week to learn and implement this blog with the first on the list, [Jekyll](https://jekyllrb.com), that way if something went wrong or I didn't like the experience I would just go onto the next one.


<h2><b> There will be Ruby,Gems and curses.</b></h2>
<h3>Installation Time: About 1 terminal session.</h3>

The Biggest pain point so far has been installing Jekyll,<span class="hl">if you are looking for a simple App or executable, this is not it </span>, Jekyll is written in Ruby, and as such it seems to prefer a Mac environment, ( haven't tried it on Windows, but it seems [possible](https://jekyllrb.com/docs/windows/#installation))  it also requires several dependencies and I had multiple conflicts that required hunting down fixes on Stack Overflow and running terminal updates and commands, so business as usual, just be aware you will have some terminal time, you like your terminal time don't you ?

<h2><b>Learning Jekyll.</b></h2>
<h3>Learning Time: (15-30) 5 minute videos</h3>

**Official Documentation** : [Jekyll's Official Documentation](https://jekyllrb.com/docs/variables/)

Great resource, but not very beginner friendly, if at first it seems inscrutable, fear not, this is your guy:

**[Thomas Bradley's Jekyill's Playlist](https://youtu.be/oiNVQ9Zjy4o?list=PLWjCJDeWfDdfVEcLGAfdJn_HXyM4Y7_k-)**   

I went over Thomas's excellent tutorials,which are both short and to the point, but got the gist of it halfway through and skimmed over the rest, if you've done any CMS or scripting development it will instantly click.

<h2><b>Github Integration.</b></h2>
<h3>Setup/Learning Time: 0-2 days</h3>

While you can use Jekyll without Github, you would be missing out on one of the coolest things ever, [free and seamless github hosting and integration of your Jekyll project or blog](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/), that's right, <span class="hl">after you setup your Jekyll site you can simply commit from your local build to your Github repo ( a special gh-pages branch ) and you are done </span>.


If what I just said made no sense, you might want to  learn and integrate Github version control into your workflow , here's a painless introduction to Github:

[GITHUB for NOOBS](https://youtu.be/1h9_cB9mPT8?list=PLqGj3iMvMa4LFz8DZ0t-89twnelpT4Ilw)


<h2><b>Codepen & Jekyll.</b></h2>

So where does Codepen fit into this static website Github hosted Jekyll business ?

In my case, I wanted a very specific look for my blog posts inspired by [Scrivener](https://www.literatureandlatte.com/scrivener.php) - an amazing writing tool, so I decided to make a couple of prototypes for my blog index and posts and then use them as templates for my Jekyll site, here they are:


<h3>The Index page:</h3>

<p data-height="265" data-theme-id="0" data-slug-hash="mEqqjg" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/mEqqjg/">Bootstrap Blog  Index Template</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3>The posts Template:</h3>

<p data-height="265" data-theme-id="0" data-slug-hash="QEOwAa" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/QEOwAa/">Bootstrap Blog Post Template</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<br />
<br />

The final templates ( layouts & includes in Jekyll's parlance) ended up a little different, but <span class="hl"> using Codepen for the initial sketch was not only a time saver, it was fun</span>

<h2><b>Adapting the prototypes:</b></h2>

To give you an example of how Jekyll works, here is the Index file that generates this blog:



{% highlight html %}
{% raw %}
---
layout: default
title: K3no.com Fron End Web Development, UI,UX Design
---

<div class="row postIndex">
  <div class ="col-sm-1"></div>
  <div class ="col-sm-10">
    <br />
    <br />
    <h2 class="blogTitle"><b>Front End & Web Development</b></h2>
    <br />

    {% for post in site.posts %}

    <div class="list-group">
      <a href="{{ site.baseurl }}{{ post.url }}" class="list-group-item">
        <h4 class="pull-right"><i>{{ post.date | date: '%B %d, %Y' }}</i></h4>
        <h2 class="list-group-item-heading"><b>{{ post.title }}</b></h2>
        <p class="list-group-item-text">{{ post.excerpt }}</p>
      </a>
    </div>

    {% endfor %}

  </div>
  <div class ="col-sm-1"></div>
</div>

{% endraw %}
{% endhighlight %}

<br />
<br />

You might be wondering where is the rest of the document and what are those curly things, well, that's how Jekyll works, the block up top is called [Front Matter](https://jekyllrb.com/docs/frontmatter/) and allows you to specify a layout ( where most of the html resides) ,declare page variables and much more, the curly things are variables that work in tandem with the folder structure to allow you to say... go over all the posts in a folder and list their titles and create post pages, there is of course a lot more to it and this is not a tutorial, but hopefully you get the idea of how your files will look.

<h2><b>A typical Jekyll workflow.</b></h2>

1. Open Github Desktop
2. From Github open project in Terminal
3. Start Jekyll in terminal
4. From Github open the project in a text editor (I like atom)
--- Sounds like a lot of work, but takes about 10 seconds in practice ---
5. Write and Create posts ( The whole site gets recreated each time you save) and lets you know through the terminal if something went wrong.
6. Preview the new pages or changes locally (in a browser on localhost:4000)
7. Commit to Github pages and changes or posts are now live.


<h2><b>Final Impressions.</b></h2>

- It took about a  week to learn and make a small blog CMS in jekyll, your learning curve might be longer or shorter depending on your previous web development experience and other factors, due to it's popularity and maturity, there are decent jekyll learning resources online.
- I wish I had used Jekyll before.
- Now I want to explore more static website generators.
- Not sure I would recommend it to non technical users or leave an average client in charge of updating a Jekyll site.
- A great almost bulletproof workflow with Codepen tests and Github integration.
- Still room for improvement, live reload, and an easier setup &  beginner documentation would be great, but if you are willing to put in a little effort <span class="hl">it is a great web development tool to get into.</span>

<br />
<br />

Drink Up !,

Keno


<img class="img-responsive" src="https://github.com/jekyll/brand/raw/master/jekyll-logo-light-transparent.png" alt="Jekyll Logo">
