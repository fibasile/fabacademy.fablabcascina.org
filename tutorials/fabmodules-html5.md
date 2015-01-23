---
title: HTML5 FabModules setup tutorial
layout: page
permalink: /tutorials/fabmodules-html5 
---


This short tutorial shows how to setup the new HTML5-based version of Fab Modules

## Find the modules

You can find the new modules at the following address

[http://mod.cba.mit.edu/mods.html](http://mod.cba.mit.edu/mods.html)


## Pre-requisites

There are some pre-requisites

- wget (apt-get install wget on a debian / ubuntu system)

- the old Fab Modules from [http://kokompe.cba.mit.edu](http://kokompe.cba.mit.edu)

- node.js & npm (download from [nodejs.org](http://nodejs.org) and follow instructions there)

- Python

- PySerial library. After getting python working, just run 

	sudo pip install pyserial 

## Download instructions

Open a terminal and create a folder where you like the fabmodules to be downloaded. 

In my case its /opt/fabmodules, and I'm creating it with sudo and I'm changing the ownership for this folder to my user :

	sudo mkdir /opt/fabmodules
	sudo chown -R fiore /opt/fabmodules

At this point make sure you have wget installed. Start downloading the first file:

	cd /opt/fabmodules
	wget http://mod.cba.mit.edu/mod_get

Now make it executable and run it:

	chmod +x mod_get
	./mod_get
	
If you followed all the instructions correctly you should now have inside /opt/fabmodules a folder named **mod.cba.mit.edu**.

	cd mod.cba.mit.edu
	

You now need to copy it alogn with the mod_server folder to /usr/local/bin, make sure you use sudo if you don't have enough privileges. Also you need to make the mod_serve file executable:

	sudo cp -R mod_serve mod_server /usr/local/bin
	sudo chmod +x /usr/local/bin/mod_serve
	
We are almost done. 

## Start  Fab Modules

You now can run the mod_serve, check /usr/local/bin is in your path:

	mode_serve &
	listening for connections from 127.0.0.1 on 12345
	
	
Finally open the index.html in your browser, and you should be going.


## Optional configuration

The file mod_settings contains the ports and speeds used for the modules operation. Make sure they match your actual devices.

You can load your mod_settings using the last menu item appearing when you open the index.html page.

 
 


