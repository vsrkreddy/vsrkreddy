---
layout: post
title: Setting Up Domain Name For Your WordPress Site and Cloudflare As DNS Provider
date: 2018-02-17 00:12:18.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
redirect_from:
  - /2018/02/17/setting-domain-name-wordpress-site-cloudflare-dns-provider/
  - /2018/02/17/setting-domain-name-wordpress-site-cloudflare-dns-provider/amp/
cardImage: Capture-1024x457.jpg
meta:
  _edit_last: '1'
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:91:"http://abyte.stream/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _the_champ_meta: a:5:{s:7:"sharing";i:0;s:16:"vertical_sharing";i:0;s:7:"counter";i:0;s:16:"vertical_counter";i:0;s:11:"fb_comments";i:0;}
  _yoast_wpseo_content_score: '60'
  _yoast_wpseo_primary_category: ''
  ampforwp_custom_content_editor: ''
  ampforwp_custom_content_editor_checkbox: ''
  ampforwp-amp-on-off: default
author:
  login: sanjaypatel2525
  email: sanjaypatel2525@gmail.com
  display_name: sanjaypatel2525
  first_name: ''
  last_name: ''
---
In my previous blog, we have covered how to setup WordPress website on Google Cloud for free.
In this blog, we are going to discuss about how we can setup a domain name for our WordPress Site and compare two main domain name registrar. Also, we will cover adding up securing and speeding up your site with CloudFlare
&nbsp;
# Why CloudFlare

* It is free
* It blocks a DDoS attack, saves your site from meltdown.
* It has its own caching, It reduces the load from your server.
* Cached content is stored in CDN which means it serves your content way faster their normal server and from nearest located CloudFlare to your end user.

# What is domain name registrar
In simple terms, domain name registrars are the entity who maintains records of the domain name. For every domain name registered with this registrar, they need to pay a fee to global central entity.  With this we can say no registrar will provide us a free domain name. Probably in the starting, they offer you a very good price like $1 or $2 but they will make sure to fill up their wallet on domain renewal time.
I spent some time to find and compare out the right register for me. Here are two which I want to share with you.
1. FreeNom.com - 1st year free, Charges $15 next year onwards.
This is good to get started as it is free and there is nothing to lose. Once you see you are doing good with your website plan compare prices and move to another domain name (Definitely your SEO will be impacted but there are workarounds. Please read my other blog on moving your site to new domain.)
2. Namecheap.com - As the name suggests they are really cheap not free but really cheap. They domain names starting from $0.48 per year and $6 for 5 year which is really good compared any other services available in the market.
My personal recommendation will be if you don't want to spend any money in the starting, go with Freenom and go with Namecheap if you thinking for the long term.

# Setting up WordPress Domain with FreeNom
* Signup and login to FreeNom.
* Go to Register a New Domain and find a domain name for you and register it.
<img class="alignnone wp-image-125 size-large" src="{{ site.baseurl }}/assets/Capture-1024x457.jpg" alt="" width="525" height="234" />
* Go to My Domains from 2 step screen and click on manage.
<img class="alignnone size-full wp-image-126" src="{{ site.baseurl }}/assets/img_5a876b6879f2f.png" alt="" />
* Go to Nameserver and select custom nameserver.  Here we change the DNS manager to CloudFlare.
Add following DNS names.  
aron.ns.cloudflare.com  
carter.ns.cloudflare.com  
<img class="alignnone size-full wp-image-127" src="{{ site.baseurl }}/assets/img_5a876c27a4870.png" alt="" />

# Setting up WordPress Domain with NameCheap
* Signup and login to NameCheap.
* Find a domain and purchase it for you.
* Go to Account Dashboard- &gt; Domain List.
<img class="alignnone size-full wp-image-128" src="{{ site.baseurl }}/assets/img_5a876ecc0807e.png" alt="" />
* Click on manage button and change DNS as mentioned below.
<img class="alignnone size-full wp-image-129" src="{{ site.baseurl }}/assets/img_5a876f309d143.png" alt="" />
This is it, Our domain name registration is complete, Now the last thing is pending is to redirect the domain name to our WordPress website site google cloud external IP.

# Setting up WordPress Domain name redirect to Google Cloud External IP
* Signup and login to CloudFlare.
* Enter your domain name here and click next, Select free plan.
<img class="alignnone size-full wp-image-130" src="{{ site.baseurl }}/assets/img_5a876ff97fd9e.png" alt="" />
* Add your WordPress website domain name and your Google Cloud External IP.
<img class="alignnone size-full wp-image-131" src="{{ site.baseurl }}/assets/img_5a8770a171bc7.png" alt="" />
You are all set, What we have achieved here,
Registered a domain name and enabled it with CloudFlare. Though Cloudflare will lessen the burden from your server with its own caching mechanism since in our previous blog we have selected Google Clouds lowest possible configuration we have to finetune further so that our site loads faster. Please read my another blog on finetuning WordPress site to work with Google Cloud F1 instance.