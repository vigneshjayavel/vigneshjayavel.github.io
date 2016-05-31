---
layout: post
title: Rails ActiveRecord Callback Chains
---

I am working with a RoR backend that is basically Rails 2.3.8 based. Yes, it is an outdated version, but still you have to get things done. ActiveRecord callbacks are one of the most powerful functionalities of the Rails ActiveRecord class. If understood correctly, they make good weapons for the developers. This is the order of callbacks in Rails 2.3.8

###Creating an Object

* before_validation
* before_validation_on_create
* VALIDATION
* after_validation
* after_validation_on_create
* before_save
* before_create
* INSERT OPERATION
* after_create
* after_save

###Updating an Object

* before_validation
* before_validation_on_update
* VALIDATION
* after_validation
* after_validation_on_update
* before_save
* before_update
* UPDATE OPERATION
* after_update
* after_save

###Destroying an Object

* before_destroy
* DELETE OPERATION
* after_destroy

##Diving deep into ActiveRecord callbacks


To dive deep into callbacks we should know the callbacks that are registered on a model.


###Getting all the callback chain methods

{% highlight ruby %}
Model.methods.select {|method| method.to_s.include? "callback_chain"}
{% endhighlight %}

This lists all the possible callback chains for a model class (no matter whether there really exists a registered callback or not)

Technically this is an array of symbols which are callback chain method names.


###Getting all the callbacks and the actual method names

Say you have a callback chain and now you need to know the methods that are part of that callback chain.
This trick will give you the exact detail

{% highlight ruby %}
Model.callback_chain_method.map(&:method)
{% endhighlight %}


###Getting all the callback chains and the callback method names

{% highlight ruby %}
Model.methods.select{|method| method["callback_chain"]}.each do |callback_chain|
	puts "####{callback_chain.to_s} : "
	puts Model.send(callback_chain).map(&:method).join("\n")
	puts "----------------"
end
{% endhighlight %}

