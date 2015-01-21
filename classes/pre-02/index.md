---
title: HTML and Static site generators
layout: lesson
subtitle: Tools and techniques to build your personal website
---

# Summary

- [HTML5 and CSS3](#html5-and-css3)
- [Javascript](#javascript)
  - [JQuery](#jquery)
  - [Node js](#node-js)
- [Web frameworks](#web-frameworks)
    - [Bootstrap](#bootstrap)
    - [Foundation](#foundation)
- [Static site generators](#static-site-generators)
    - [Markdown](#markdown)
    - [Jekyll](#jekyll)
    - [Octopress](#octopress)
    - [Pelican](#pelican)
    - [Pandoc](#pandoc)
- [Hosting your site](#hosting-your-site)
    - [Web hosting](#web-hosting)
    - [GitHub Pages](#github-pages)
    - [Fab Academy Archive](#fab-academy-archive)
- [Assignments](#assignments)

## HTML5 and CSS3

Html is the basis of the world wide web. With [HTML5]() a lot of features were introduced into
the language, most importantly the [Canvas](http://en.wikipedia.org/wiki/Canvas_element) element,
native [HTML5 Video](http://www.html5rocks.com/en/features/multimedia) (no more flash),
and a lot of new tags for [semantic](http://diveintohtml5.info/semantics.html) formatting of content.

Where HTML describes the content of a web page or application, CSS describes its looks.
With the new CSS3 you can style everything, adding shadows, creating gradients and
even radically changing the content style based on the screen size and orientation.

[**Mobile-first responsive design**](http://www.html5rocks.com/en/mobile/responsivedesign/)
is the current trend in web design. This means making webpages which can look good
on mobile devices and on desktops too from the same source.

Since 95% of communication on the internet today is based on this technology you need
to master it. At least to the point where you can write on your own a webpage, style
and publish it.

Great links to learn more about HTML5 and CSS3:

- Dive into html5
[http://diveintohtml5.info](http://diveintohtml5.info)

- Html5up
[http://html5up.net](http://html5up.net)

- CSS3 Generator
[http://css3generator.com](http://css3generator.com)

- HTML5 Rocks
[http://www.html5rocks.com/en/](http://www.html5rocks.com/en/)

## Javascript

When you need to add some interactivity to your webpages you can do so using Javascript.
This language has been around since the beginning of the web, and has evolved now into
a standard, so all browsers support it.

With javascript you can program buttons, tabs, dialogs, create games and interfaces of
all kind.

A great book on learning Javascript, and a good introduction to programming is:

- Eloquent Javascript
[http://eloquentjavascript.net](http://eloquentjavascript.net)

### JQuery

JQuery is a library for Javascript which allows to manipulate web content in a very convenient
way. 99% of modern web applications use jQuery as their basis.

You can learn jQuery together with Javascript by creating some small web application living in
the browser only.

Learning jQuery is easy, follow any of these guides:

- [http://learn.jquery.com](http://learn.jquery.com)
- [http://www.codecademy.com/en/tracks/jquery](http://www.codecademy.com/en/tracks/jquery)

### Node JS

Node JS allows to use Javascript to develop web applications which run on the server.
This is similar to what you can do with PHP, but much more stable and secure.

Also using Javascript for both the client and the server makes it much easier to work
as we don't need to use different languages. Also you can use the same code for both.

Node.js is used often with the Express.js framework, which makes it easy to write
web services, do authentication etc.

Learn more about Node.js on [http://nodejs.org](http://nodejs.org) and about Express.js [http://expressjs.com](http://expressjs.com)

## Web frameworks

When developing web pages and web apps you usally write over and over the same code,
for example you always have a navigation bar, you need to have buttons, panels,
dialogs, forms etc.

In the old days you had either to do this every time, or to write yourself some
kind of library of reusable components in order to save some work.

Today there are several frameworks which already provide you with some pre styled
elements that you can just copy and paste to use directly into your pages.

### Bootstrap

Bootstrap is a free collection of tools for creating websites and web applications. It contains HTML and CSS-based design templates for typography, forms, buttons, navigation and other interface components, as well as optional JavaScript extensions.

You can download the Bootstrap distribution from [http://getbootstrap.com](http://getbootstrap.com)

Boostrap can be seen as several components:

- The [CSS styles](http://getbootstrap.com/css/) dealing with general typography and how text is styled. The Bootstrap CSS allows also to format tables, forms, button, images, and so on.

- The [Reusable components](http://getbootstrap.com/components/) which include icons, toolbars, navigation lists, dialogs, breadcrumbs, etc. 

- The [Javascript components](http://getbootstrap.com/javascript/) like tab panels, collapsible elements, modal dialogs, etc.

It's not mandatory to use components if you don't like, for example you might just use the grid. 

On top of Bootstrap you can use several custom themes, like one contained in [http://bootswatch.com](http://bootswatch.com), where you simply add a new CSS over the one provided by
Bootstrap to get new styling.

Many sites also provide snippets of code for common use cases built using Bootstrap, one of these is [http://snipplicious.com](http://snipplicious.com). Search for "bootstrap snippets" to find more.  

Finally if you like to have a complete template, including bootstrap plus some ready to use pages you can check [http://startbootstrap.com](http://startbootstrap.com).

A great resource for learning how to use Bootstrap is to watch:

Learn Twitter Bootstrap in 2 Hours:
[https://www.youtube.com/playlist?list=PLKlA1QwYBcmcEUUBSmkl8_kgwn-_zuy-W](https://www.youtube.com/playlist?list=PLKlA1QwYBcmcEUUBSmkl8_kgwn-_zuy-W )


### Foundation

Foundation is another popular alternative to Bootstrap providing similar elements. Some people prefer it because is less bloated and eventually faster. 

You can download Foundation from [http://foundation.zurb.com](http://foundation.zurb.com)

The [Foundation Getting Started Guide](http://foundation.zurb.com/docs/) provides documentation on the Framwework.

In particular you have access to:

- The Grid
- Buttons
- Navigation
- Forms
- Plugins with a number of Widgets 

On [Zurb University](http://patterntap.com/code) you can find a number of ready to use snippets and templates based on Foundation framework.


## Static site generators

If you tried to develop a full static site with or without one of the frameworks mentioned above, you will have noticed that a lot of the
code is repeated over and over.

For example a website organized like the following:

	-----   Header ------
	----- Navigation ----
	----    --------
	side    content
	bar
	----    -------
	-------  Footer -------

Requires you to duplicate for each page the Header, Navigation, Sidebar and Footer Blocks. 
Furthermore you have to keep track of all links and make sure to update them every time something changes on the site. 

Usually you can solve these problems using a Content Management System (CMS) like Wordpress or Drupal. These software packages come with templates
that take care of most of these tasks. And the dynamic parts of your website, like menus are dynamically rendered from a database.
But CMS software is difficult to maintain and even more to keep secure, and quite slow too. Malicious users can hack your site or in the best case put it offline.
And it usually takes few seconds before your homepage shows up.

On the other side static sites are very fast, nobody can hack them, there is no security backdoor, and they don't need any upgrade during time. Plus they're small to download, and you can work on them offline too.

Static site generators try to bring you the best of both worlds. Like CMS you have templates, so you can focus on the content and compose pages from reusable snippets. And they produce static sites exactly like you would do by hand, just better, because it's difficult to have broken links and so on.

Static site generators work like this:

1) You start with a basic folder structure, with folders where you put your pages, usually as Markdown documents, and folders containing templates and includes.
2) You can change the style of the site by editing templates and CSS 
3) You add in your content
4) You "compile" the site, producing a "static" folder 
5) You copy the contents of the static folder on your server, either by FTP, SSH or Version control.

Every time you want to update your site, you just do steps 3) to 5). 


### Markdown 

Markdown is not a site generator, but we talk about it because most site generators use this as one of the accepted formats for writing content.

This page you are reading is written in Markdown for example. See the [source](https://raw.githubusercontent.com/fibasile/fabacademy.fablabcascina.org/master/classes/pre-02/index.md) for an example of Markdown.

Basically Markdown is made of text files that, when compiled, can be converted in HTML and several other formats. 

Additionally they are quite readable by themselves, as the formatting rules are made to allow people to read it as is without any conversion.

A full guide to Markdown formatting is at [http://daringfireball.net/projects/markdown/syntax](http://daringfireball.net/projects/markdown/syntax), but
you can also find convenient to read the [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

Many text editors support Markdown natively, and they add a nice preview panel. 

Check out [http://dillinger.io](http://dillinger.io) or search for "Markdown Editor", you will find a ton. Once you learn it, you will never use MS Word again.

### Jekyll

Jekyll is the most popular Markdown based web site generator. You can download it from [http://jekyllrb.com](http://jekyllrb.com).

It might be tricky to install because it requires recent [Ruby](http://ruby-lang.org) and [Rubygems](https://rubygems.org).

Once you have all of this installed: 
	
	sudo gem install jekyll
	jekyll new my-awesome-site
	jekyll serve
	
At this point you can open your browser to [http://localhost:4000](http://localhost:4000) and see your site preview live.
Once you are done with your site you can create a final static version of it with

	jekyll build
	
This will make a **_site** folder containing your site code.

Jekyll will generate a folder structure like the following

	_config.yml
	_includes
	_layouts
	_posts
	_sass
	about.md
	css
	feed.xml
	index.html

- _config.yml is where you edit your site config, things like the title, your name etc. You can also define new vars here and show them into the templates
- _includes contains the parts of the templates which are repeated over and over. You will include them in your template
- _layouts contains the main layout of the site and you can add other, for each different page type. In this site I have a layout for news, one for pages and one for classes
- _posts is where you put the "news" or "blog". These are different from pages because are compiled into date - based folders and shown in the homepage in date order.
- the about.md and any other page you want to create are plain text files. 

The only thing that makes about.md special is the header on top of the file:

	---
	layout: page
	title: FabAcademy 
	permalink: /about/
	---

The layout row tells which file from the _layout folder should be used for this page. The title is the title for this page, shown also in the top menu. Finally the permalink tells which address should be associated with the page.

You can also use folders to define your pages, putting an index inside it: for example if you want a tutorials page, you could create a tutorials folder and an index.md page into it.

Jekyll is very popular, and some people created plugins and themes for it. If you want to use a theme, or to develop your own, you can find lots of good examples at [http://jekyllthemes.org](http://jekyllthemes.org).

The [Freelancer Theme](https://github.com/jeromelachaud/freelancer-theme) is interesting because it uses bootstrap.

To use Freelancer, clone its git repository and just run jekyll serve inside the created folder.


### Octopress

Octopress is directly derived from Jekyll. It adds some nice features which make it more suited for a blog, like search, a post calendar, source-code synthax coloring, etc.

This is [Octopress](http://octopress.org/docs/setup/) site. Instructions for setting it up are [here](http://octopress.org/docs/setup/).

As of now a new version of Octopress is in final development stages. See [here](https://github.com/octopress/octopress)

### Pelican

If you are looking for an alternative to Jekyll / Octopress, or have trouble with Ruby you can have a look at [Pelican](http://blog.getpelican.com).

This tool is based on Python language, which makes it a bit less prone to software version troubles.

As explained in the Pelican great [documentation](http://docs.getpelican.com/en/3.5.0/quickstart.html#installation) you can install it with:

	pip install pelican markdown
	mkdir -p ~/projects/yoursite
	cd ~/projects/yoursite
	pelican-quickstart
	
Pelican doesn't come with much example content. You need to create a post befor using it.  Create a file ~/projects/yoursite/content/test.md

	Title: Title
	Date: 2010-12-03 10:20
	Category: Review

	This is a test

Then generate the site with

	pelican content
	
Pelican doesn't have a built in webserver. But with Python you can run one easily. Go into the site folder and run:

	cd ~/projects/yoursite/output
	python -m SimpleHTTPServer
	
then open the browser to [http://localhost:8080](http://localhost:8080)

Pelican also comes with a number of [themes](https://github.com/getpelican/pelican-themes)  

### Pandoc

PanDoc is not stricly a site generator but a multi purpose tool for converting documents from one format to another.
If you write your content in Markdown, you can use Pandoc to create HTML, PDF, DOC, RTF, etc. 

You can download PanDoc from the site [http://johnmacfarlane.net/pandoc/](http://johnmacfarlane.net/pandoc/)

These are the supported file format, and PanDoc converts FROM any of these TO any of these. 

- HTML formats: XHTML, HTML5, and HTML slide shows using Slidy, reveal.js, Slideous, S5, or DZSlides.
- Word processor formats: Microsoft Word docx, OpenOffice/LibreOffice ODT, OpenDocument XML
- Ebooks: EPUB version 2 or 3, FictionBook2
- Documentation formats: DocBook, GNU TexInfo, Groff man pages, Haddock markup
- Page layout formats: InDesign ICML
- Outline formats: OPML
- TeX formats: LaTeX, ConTeXt, LaTeX Beamer slides
- PDF via LaTeX
- Lightweight markup formats: Markdown, reStructuredText, AsciiDoc, MediaWiki markup, DokuWiki markup, Emacs Org-Mode, Textile

If you don't like the options above for creating your site, this could be a useful tool to write your own. :)
Someone [did it already](https://github.com/wcaleb/website)

## Hosting your site

### Web hosting

Static sites can be hosted basically everywhere. Starting from any Hosting providers, your Dropbox Public Folder, to Amazon S3 Buckets.

You can easily setup your own webserver using [Apache](http://www.apache.org) or [Nginx](http://nginx.org) and a machine rented from a Virtual Server provider like [DigitalOcean](http://digitalocean.com), [Rackspace](http://www.rackspace.com), [Windows Azure](http://azure.microsoft.com/it-it/) or [Amazon EC2](http://aws.amazon.com/ec2/).

Most of the time you will transfer your content using [FTP](http://en.wikipedia.org/wiki/File_Transfer_Protocol), [SFTP](http://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol), [RSYNC](http://en.wikipedia.org/wiki/Rsync). But if you have shell acess you can also use Git or Mercurial.

### Github Pages

GitHub offers a great free static site hosting service. You can have a personal or a per-project static site. 

Personal site works likes this:

- You create a repository on Github named yourusername.github.io (replace yourusername with your username)  
- You commit and push your static site to this repository
- Your site is visible at yourusername.github.io

Strongly recommended!

More info on [GitHub Pages](https://pages.github.com) here.

### Fab Academy Archive

Fab Academy hosts personal sites using Mercurial. More on this in the following weeks. Get your site ready by then!!

## Assignments

- Get familiar with HTML and CSS, create some pages
- Create your on site with one of the tools mentioned here, creating at least and About page on you
- Host and upload your site using GitHub Pages
- Extra credit, create your own theme for your site

**Extra**

- Start thinking about your final projects!!!

