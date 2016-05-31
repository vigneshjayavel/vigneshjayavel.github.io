---
title: Cutting costs on servers - Switching from Linode VPS to DigitalOcean Cloud - A developer's experience
author: vigneshjayavel
description: 
post_id: 267
created: 2013/06/26 23:25:21
created_gmt: 2013/06/26 23:25:21
comment_status: open
post_name: cutting-costs-on-servers-switching-from-linode-vps-to-digitalocean-cloud-a-developers-experience
status: publish
layout: post
---

## Cutting costs on servers - Switching from Linode VPS to DigitalOcean Cloud - A developer's experience

A couple of months back I subscribed to Linode's vps service for an app that I'm working on. Linode is super-awesome. At $20/month I got a VPS with 1gig of memory, 24gigs of storage, scalability of XEN middleware and full root access! Initially I was overwhelmed by the "raw power" it provides. It served as an all-in-one solution satisfying the geek in me by providing a robust web-hosting platform for my hobby projects, my private git repo setup, my VPN (You know, I 'm a student and my college network is definitely filtered! :P ) . VPS is an indispensable tool for any developer. I had funding to subscribe to Linode's service for around 6 months. I thought it would be wiser to step down (after 2 months of awesome life with Linode) to a much affordable server solution as I could save few dollars by cutting costs on servers during the "dev" stage. After a lot of research online I finally settled for DigitalOcean's $5 plan that gives 512mb memory and a 20gigs of SSD storage (Wow! this should hopefully quench the app's thirst in the incubation period  B-) ). Pretty much similar to Linode from what I have read from other dev blogs, DigitalOcean is for the rest of us! The cheapest VPS on the planet AFAIK. Now I 'm on a migration process. Thanks to the lovely Linux Terminal, "rcp" makes it easier for me to copy files from Linode to DigitalOcean's "droplet" ! I 'm few steps behind completing the LEMP (linux-nginx-mysql-php) setup. All that is left to be done is setting up the nginx rewrite rules to run my CodeIgniter app without any glitch. :)