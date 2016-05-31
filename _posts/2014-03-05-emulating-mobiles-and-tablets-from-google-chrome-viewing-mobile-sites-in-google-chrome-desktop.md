---
title: Emulating mobiles and tablets from Google Chrome (Viewing mobile sites in Google Chrome desktop)
author: vigneshjayavel
description: 
post_id: 398
created: 2014/03/05 18:43:59
created_gmt: 2014/03/05 13:13:59
comment_status: open
post_name: emulating-mobiles-and-tablets-from-google-chrome-viewing-mobile-sites-in-google-chrome-desktop
status: publish
layout: post
---

## Emulating mobiles and tablets from Google Chrome (Viewing mobile sites in Google Chrome desktop)

Web developers are always in need of testing how their applications look and behave in different view ports. In this era of responsive design and "mobile-first" approach, developers should make sure that their applications are usable by their target audience. There are many workarounds to test a web application/page for multiple view ports. Resizing the browser window, using a target device's emulator, running the app in the target device itself,.. Thanks to chrome for providing the super powerful Developer Tools console. Web developers can now test their applications in emulators for various devices from within Google Chrome itself. Steps : 1\. Load your web app (open the desired app/page in chrome) 2\. Ctrl + shift + i 3\. Click the button at the right corner of the developer tools ![Image](http://vikkiandtheweb.files.wordpress.com/2014/03/capture.png?w=25) 4\. You should see a console popping from the bottom of the tools window. Click the "Emulation" tab. 5\. Set the Device, User Agent and Screen settings based on your target device. This is how google home page looks on Nexus 5 emulator with user agent set as Android 4.0.2![Image](http://vikkiandtheweb.files.wordpress.com/2014/03/capture1.png?w=574) Note : This feature allows you to spoof User Agent, locations, accelerometer and even touch gestures that are supported in the emulated device. Tried and tested on Google Chrome Version 33.0.1750.146 m (Windows 7 x64)

