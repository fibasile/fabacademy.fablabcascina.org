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

You can learn Python in several ways. 

The best route of course is to get some python project and study it. But there are thousands of free tutorials and books to learn the language. 

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


## Installing Python Libraries

For installing any Python library we can use PIP the Python package manager. 

If you don't have it, you can install Pip downloading [get-pip.py](https://bootstrap.pypa.io/get-pip.py) and typing in your terminal:

	sudo python get-pip.py

On Debian and Ubuntu you might prefer to use your package manager

	sudo apt-get install python-pip
	
Once installed, using pip is very easy. Please note you might need to use **sudo** before pip for getting superuser privileges:

	pip install <packagename>
	
will install packages,

	pip search <string>
	
will look for packages matching a string.

Very often when you download Python projects from Github, they come with a requirements.txt. In this case is easy to install all their dependencies by running

	pip install -r requirements.txt

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

We can use PyQT/PySide for this. Let's start by installing PySide (also you need Qt 4.8, see [this page](http://qt-project.org/wiki/Setting_up_PySide)):

	pip install pyside
	
**NOTE** on OSX you might need to use homebrew and then run pyside_postinstall.py -install 

We can now code basic apps. 

For example create a main.py in some folder containing this code:

	import sys
	from PySide import QtGui


	app = QtGui.QApplication(sys.argv)

	hello = QtGui.QPushButton("Hello world!")
	hello.resize(100, 30)

	hello.show()

	sys.exit(app.exec_())
	
And run it like this:
	
	python main.py

This will show a very tiny button with "Hello world" written on it. Yes! You wrote your first desktop app in Python and successfully installed pyside.

To progress further, the best way is to study working code. You can clone the following repository

[https://github.com/PySide/Examples](https://github.com/PySide/Examples)
	  
In the examples/tutorial folder you can find several steps t2,t3, etc. with increasingly complex features till you build a complete game.

Finally out the example in the examples/tutorial/addressbook folder. This is the python version of this [tutorial](http://doc.trolltech.com/tutorial.html)
	  
## Python for Web apps

One of the largest user base for Python is web developers. Python was used for this since 2000 and many frameworks are built for this purpose.

The main frameworks for web development in Python today are:

- [Flask](http://flask.pocoo.org)
- [Web.py](http://webpy.org)
- [TurboGears](http://turbogears.org)
- [Django](https://www.djangoproject.com)
  
### A web app example

We can use Flask for a basic example. Again to install flask, it is enough to type:

	pip install flask
	
At this point we can code our first web app, call it webapp.py:

	from flask import Flask
	app = Flask(__name__)

	@app.route("/")
	def hello():
	    return "Hello Fab Academy!"

	if __name__ == "__main__":
	    app.run()
		 
And run it:

	python webapp.py

Now open your web browser on http://127.0.0.1:5000/

If all works as expected we are serving our first basic webpage!

Now let's check a more complex example. A twitter clone built with Flask and SQLite, a file based database.

Download the [latest Flask release](http://pypi.python.org/packages/source/F/Flask/Flask-0.10.1.tar.gz) from the site. 
Uncompress the archive and go inside the examples/minitwit folder.

Before using the app we need to init its database, launch python on his own

	python
	Python 2.7.5 (default, Mar  9 2014, 22:15:05) 
	[GCC 4.2.1 Compatible Apple LLVM 5.0 (clang-500.0.68)] on darwin
	Type "help", "copyright", "credits" or "license" for more information.
	>>>
	
And type

	>>>from minitwit import init_db; init_db()
	
Now we are using the python **interpreter**. Everything we write in our files in fact could be written interactively line by line. This is great for debugging or testing code while we write it.

Now hit CTRL-D to exit the Python Shell. We can now run our app:

	python minitwit.py

Open your browser on http://127.0.0.1:5000/

Now you can see your twitter clone running. Open the minitwit.py to discover how it works.
	
Check out this page for a [full tutorial on flask](http://flask.pocoo.org/docs/0.10/tutorial/)

## Python for Graphic apps 

Python is great for prototyping games and graphical apps. 

Some frameworks for this are:

- [Kivy](http://kivy.org)
- [PyGame](http://pygame.org/)
- [PyGlet](http://www.pyglet.org/)
- [Panda3D](https://www.panda3d.org/)

###A graphic app example

We can use for example Kivy as this is a modern and well documented framework. Some examples of apps developed with it can be found in the [Gallery](http://kivy.org/#gallery).

Install Kivy from the [download page](http://kivy.org/#download). Documentation can be downloaded as [pdf](http://kivy.org/docs/pdf/Kivy-latest.pdf)

Kivy is a bit different from traditional graphic framework because it tries to simplify (a lot) the life of the programmer. It does this by introducing
a description language for defining the GUI, the KV Language.

The [Pong Game](http://kivy.org/docs/tutorials/pong.html) tutorial is a great starting point for learning how to use this framework. 

Source code is available inside the examples/tutorials/pong folder of the Kivy distribution.

	cd examples/tutorials/pong
	kivy main.py

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
	
	