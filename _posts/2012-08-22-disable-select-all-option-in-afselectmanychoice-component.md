---
title: Disable "select-all option" in af:selectManyChoice component
author: vigneshjayavel
description: 
post_id: 55
created: 2012/08/22 12:12:01
created_gmt: 2012/08/22 12:12:01
comment_status: open
post_name: disable-select-all-option-in-afselectmanychoice-component
status: publish
layout: post
---

## Disable "select-all option" in af:selectManyChoice component

af:selectManyChoice is a multi-select box that allows you to select more than 1 option at any instance. In a af:selectManyChoice component by default we get options like 

  * all
  * option1
  * option2
  * ........
  * ......
What if we need to hide or disable the "all" option which shows up by default?? **Solution** set the "selectAllVisible" attribute as "false" in the af:selectManyChoice component **Example** <af:selectManyChoice label="#{bindings.SomeVO.label}" id="sml1" autoSubmit="true" value="#{SomeBean.someValue}" valueChangeListener="#{SomeBean.someValueChanged}" _selectAllVisible="false"_ > <f:selectItems value="#{bindings.SomeAttr.someKey}" id="si11"/> </af:selectManyChoice>