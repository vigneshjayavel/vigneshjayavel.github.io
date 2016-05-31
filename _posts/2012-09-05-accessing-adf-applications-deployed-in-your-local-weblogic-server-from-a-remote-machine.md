---
title: Accessing ADF applications deployed in your local Weblogic server from a remote machine
author: vigneshjayavel
description: 
post_id: 72
created: 2012/09/05 11:16:18
created_gmt: 2012/09/05 11:16:18
comment_status: open
post_name: 72
status: publish
layout: post
---

## Accessing ADF applications deployed in your local Weblogic server from a remote machine

Once we deploy our app in our local Weblogic server, by default we get our application accessible using an app-url like http://localhost:7101/myApp Using ipconfig we need to find the IP of our machine say the IP is 10.1.1.2 Then the app-url has to be something of the form http://yourIP:WlsPort/myApp like http://10.1.1.2:7101/myApp But this will result in some "The connection has timed out" error when tried to access The solution : 1.open your weblogic server console http://localhost:7101/console 2.open server settings found in Environment pane ![](http://vikkiandtheweb.files.wordpress.com/2012/09/capture2.png) 3.Open your server (There may be a list of servers in case you are using both integrated and standalone WLS) in which your App is deployed. 4.In Listen Address, enter your IP and save 5.Stop the running server 6.Open JDeveloper 7.View->Application Server Navigator->right click on the server->Properties->Config tab 8.Enter your IP in Weblogic hostname field ![](http://vikkiandtheweb.files.wordpress.com/2012/09/capture11.png) 9.Start your server and deploy the app. Now you can share your app running at your machine with anyone with the app-url http://10.1.1.2:7101/myApp
