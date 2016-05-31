---
title: Fixing java.lang.OutOfMemory Java Heap Space error in JDeveloper
author: vigneshjayavel
description: 
post_id: 63
created: 2012/08/27 09:57:36
created_gmt: 2012/08/27 09:57:36
comment_status: open
post_name: fixing-java-lang-outofmemory-java-heap-space-error-in-jdeveloper
status: publish
layout: post
---

## Fixing java.lang.OutOfMemory Java Heap Space error in JDeveloper

You can fix this bug in JDeveloper using the following steps 1.Search for _ide.conf_ and _jdev.conf_ in you JDeveloper installation folder 2.In ide.conf file, make sure the following properties are set exactly the same **AddVMOption  -Xmx940M** **AddVMOption  -Xms128M** 3.In jdev.conf file, make sure the following properties are set exactly the same **AddVMOption  -XX:MaxPermSize=356M** 4.You also need to disable the SVN versioning system that is built into JDeveloper (This built-in svn is very buggy and consumes a lot of memory. You can use some standalone SVN clients such as TortoiseSVN for versioning) Follow these steps to complete the process, In **JDeveloper -> Choose Versioning menu -> Choose Configure -> Uncheck "Versioning support for Subversion"** ![Image](http://vikkiandtheweb.files.wordpress.com/2012/08/capture.png?w=355)
