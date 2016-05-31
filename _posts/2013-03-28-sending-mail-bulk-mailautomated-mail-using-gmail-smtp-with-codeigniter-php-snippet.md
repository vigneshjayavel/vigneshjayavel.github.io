---
title: Sending mail (Bulk-mail/automated mail) using GMail smtp with CodeIgniter - PHP Snippet 
author: vigneshjayavel
description: 
post_id: 226
created: 2013/03/28 09:53:29
created_gmt: 2013/03/28 09:53:29
comment_status: open
post_name: sending-mail-bulk-mailautomated-mail-using-gmail-smtp-with-codeigniter-php-snippet
status: publish
layout: post
---

## Sending mail (Bulk-mail/automated mail) using GMail smtp with CodeIgniter - PHP Snippet 

After a long struggle I found out that the following code works perfectly (even in your localhost) using the CodeIgniter email Helper. You can now send bulkmails using your gmail account!

[code language="php"] $config = Array('smtp_user' => 'yourmail@gmail.com',    'smtp_pass' => 'yourpassword', 'protocol'=> 'smtp', 'smtp_host'=> 'ssl://smtp.googlemail.com', 'smtp_port'=> '465', 'smtp_timeout'=>'30', 'charset'=> 'utf-8', 'newline'=>"\r\n"); $CI = &get_instance(); $CI->load->library('email', $config); $CI->email->from('yourmail@gmail.com', "yourname"); $CI->email->to($emailData['to']); $CI->email->subject($emailData['subject']); $CI->email->message($emailData['message']); try{ $CI->email->send(); }catch(Exception $e){ echo $e->getMessage(); } [/code]


