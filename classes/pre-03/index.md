---
title: Introduction to the Python programming language
layout: lesson
subtitle: A batteries-included crash course
---


## Summary

- [Why Python](#why-python)
- [Learning Python](#learning-python)
- [Python for Desktop apps](#python-for-desktop-apps)
- [Python for Web apps](#python-for-web-apps)
- [Python for Graphic apps](#python-for-graphic-apps)
- [Python for Embedded systems](#python-for-embedded-systems)
- [Assignments](#assignments)


## Why Python

Python is one of the most powerful yet easy programming languages. It's used everywhere from web apps to system software (Dropbox anyone?), to videogames and even in embedded systems.

What makes Python so unique:

- beautiful synthax: it's very difficult to write bad python code, you need to indent the code or it won't compile for instance. 
- batteries included: there's a wealth of libraries for practically everything. Every web service, every system function, everything.
- very expessive: things that usually take hundreds of lines of code usually can be written in ten lines of python code.
- productive from day one: you don't need to master the language to start writing useful code.

Python is today used for teaching programming, so it's also a great language for those who never programmed before. 

## Learning Python

You can learn Python in several ways. The best route of course is to get some python project and study it. 

But there are thousands of free tutorials and books to learn the language. 

Some useful resources:
- [Learn Python in 10 minutes](http://www.stavros.io/tutorials/python/)
- [Official Python tutorial](https://docs.python.org/2/tutorial/)
- [Learn Python](http://www.learnpython.org) this is an interactive web-based python tutorial
- [The Hitchhiker’s Guide to Python!](http://docs.python-guide.org/en/latest/)

And some books
- [Learn Python the Hard Way](http://learnpythonthehardway.org/book/) great online free book
- [Learning Python from Oreilly](http://shop.oreilly.com/product/0636920028154.do) great book, ask me for it.
- [Programming Python from Oreilly](http://shop.oreilly.com/product/9780596158118.do) great book, ask me for it.


## Installing Python

You can install Python on basically anything.

- [OSX](http://docs.python-guide.org/en/latest/starting/install/osx/) 100% you already have python
- [Windows](http://docs.python-guide.org/en/latest/starting/install/win/)
- [Linux](http://docs.python-guide.org/en/latest/starting/install/linux/) 99% you already have python


## Python for Desktop apps

Python while a bit slow can be really a good introduction for writing desktop applications.

Some important open source applications are written in python. Like [Inkscape](http://inkscape.org). 
Other applications use Python as a "scripting language", exposing much of their functionality to python plug-ins. 
One of them is [Blender](blender.org).

In order to write Python Desktop apps you need to rely on some GUI framework. Luckily there are plenty of GUI frameworks for the Python language!!

Multi platform frameworks:

- [PyQT](http://www.riverbankcomputing.co.uk/software/pyqt/intro) and [PySide](http://qt-project.org/wiki/PySideDownloads/)
- [PyGTK](http://www.pygtk.org)
- [wxPython](http://www.wxpython.org)
- [TCL/TK TKInter](https://docs.python.org/3/library/tkinter.html)

Mac only
- [PyObjC](https://pythonhosted.org/pyobjc/)
- [Cocoa](http://blog.adamw523.com/os-x-cocoa-application-python-pyobjc/)


### A desktop app example

We can use PyQT for this. 

## Python for Web apps

One of the largest user base for Python is web developers. Python was used for this since 2000 and many frameworks are built for this purpose.

The main frameworks for web development in Python today are:

- [Flask](http://flask.pocoo.org)
- [Web.py](http://webpy.org)
- [TurboGears](http://turbogears.org)
- [Django](https://www.djangoproject.com)
  
### A web app example

We can use Flask for a basic example.

## Python for Graphic apps 

Python is great for prototyping games and graphical apps. 

Some frameworks for this are:

- [Kivy](http://kivy.org)
- [PyGame](http://pygame.org/)
- [PyGlet](http://www.pyglet.org/)
- [Panda3D](https://www.panda3d.org/)

###A graphic app example

We can use for example Kivy as this is newer and well documented. Install Kiver from the [download page](http://kivy.org/#download).

## Python for Embedded systems

Pyton by chance is the [language of choice of the Raspberry PI](http://www.raspberrypi.org/tag/python/). 
For this reason you can find python preinstalled on the [Raspbian Distro](http://www.raspbian.org), and there are lots of libraries to program every aspect of the Raspberry with it.

But there are also ports of the Python language for embedded systems. This will be useful for your Embedded programming assignment for instance :)

- [Python on a chip](https://code.google.com/p/python-on-a-chip/)
- [PyMite](https://wiki.python.org/moin/PyMite)


## Assignments

- Download and install python
- Write your first app in Python. This could be either a:
	1. A Web app: create a markdown editor. You can use your bootstrap knowledge and some existing component like [Epic Editor](http://epiceditor.com). The app should be able to save the pages you create on the filesystem.
	2. Desktop app: make a Git app. The app should show you the files changed in a repository, allow to add and commit them.
	3. Game: make a breakout or tetris clone. Don't copy the code from someone else, or I'll notice, promise.
	
	