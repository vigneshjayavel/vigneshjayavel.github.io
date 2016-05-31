---
title: Select top n records from a table (Oracle)
author: vigneshjayavel
description: 
post_id: 10
created: 2012/08/08 03:38:02
created_gmt: 2012/08/08 03:38:02
comment_status: open
post_name: select-top-n-records-from-a-table-oracle
status: publish
layout: post
---

## Select top n records from a table (Oracle)

select * from table_name where rownum <= :n ; /* n is the number of records you need to fetch */