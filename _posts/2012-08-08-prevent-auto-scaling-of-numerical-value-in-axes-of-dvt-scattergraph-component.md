---
title: Prevent auto-scaling of numerical value in axes of dvt scattergraph component
author: vigneshjayavel
description: 
post_id: 20
created: 2012/08/08 10:59:54
created_gmt: 2012/08/08 10:59:54
comment_status: open
post_name: prevent-auto-scaling-of-numerical-value-in-axes-of-dvt-scattergraph-component
status: publish
layout: post
---

## Prevent auto-scaling of numerical value in axes of dvt scattergraph component
{% highlight xml %}
	<dvt:y1Axis> 
		<dvt:numberFormat scaleFactor="SCALEFACTOR_NONE" thousandSeparator=""/> 
	</dvt:y1Axis> 
	/* for eg. This tag populates data in the YAxis of the scatterGraph. If the value populated is like 500000000000 it will be auto-scaled as 50000M. To prevent this use scaleFactor="SCALEFACTOR_NONE". Also, numerical values will be comma separated like 500,000,000,000. To prevent this use thousandSeparator="" */
{% endhighlight %}