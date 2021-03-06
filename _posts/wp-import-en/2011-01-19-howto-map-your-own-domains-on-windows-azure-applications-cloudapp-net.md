---
layout: post
title: "HowTo: map your own domains on Windows Azure Applications (*.cloudapp.net)"
date: 2011-01-19 20:16
author: CI Team
comments: true
categories: [HowTo]
tags: [Windows Azure]
language: en
---
{% include JB/setup %}

  <p align="left"><img style="background-image: none; border-bottom: 0px; border-left: 0px; margin: 0px 10px 10px 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" align="left" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb322.png" width="188" height="73" />If you already successfully deployed a Windows Azure Application and turned it on "active" you will get an URL after the pattern "Name.clodapp.net" for less. But how is it possible to show "name.de or "<a href="http://www.name.de">www.name.de</a>" on my application? The (short) answer:</p>  

<p><b>The magic key is transmission and "CNAME"</b></p>
<p><strong>Scenario: We already have our app on azure and all that we want now is to add the right domain. Our TestApp.cloudapp.net should be able to call with testapp.de.</strong></p>
<p>My domains are at the moment on Hosteurope and there exists a kind of domain administration (like on every provider):</p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image310.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image3_thumb.png" width="503" height="290" /></a></p>
<p><u>The first entry includes this:</u></p>
<p><u></u></p>
<p><a href="http://testapp.de">http://testapp.de</a> shows this IP</p>
<p>The problem: We don´t know the IP of Azure. So either you enter a (not Azure-) machine or you set up a transmission rule with the help of the Hoster. </p>
<p>If you decide to work with you own machine (what´s stupid in my opinion but so what ;) ) it´s an easy way to transmit to another address in IIS 7. You do so here:</p>
<p><u>T<img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb324.png" width="398" height="283" /></u></p>
<p><u><a href="{{BASE_PATH}}/assets/wp-images-en/image810.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image8_thumb.png" width="240" height="197" /></a></u></p>
<p><u>the second entry is interesting</u></p>
<p><u></u></p>
<p>Here I´m going to define a <a href="http://en.wikipedia.org/wiki/CNAME_record">CNAME</a> like <a href="http://testapp.de">http://testapp.de</a> - a CNAME just works if you have a "Subdomain". The CNAME just points to testapp.cloudapp.net.</p>
<p><b>Requestflow:</b></p>
<p><a href="http://testapp.de">http://testapp.de</a> -&gt; is transmitted to <a href="http://www.testapp.de">http://www.testapp.de</a> and this is transmitted to the Azure platform. But it won´t work without www or another subdomain (also app.testapp.de would be work).</p>
<p>But the cloudapp.net is NEVER shown to the user. </p>
<p>That´s it! <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-smile" alt="Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-smile1.png" /></p>
<p>More Informations:</p>
<p>- <a href="http://blog.smarx.com/posts/custom-domain-names-in-windows-azure">Custom Domain Names in Windows Azure</a></p>
<p>- <a href="http://blog.smarx.com/posts/using-the-new-windows-azure-cdn-with-a-custom-domain">Using the new Windows Azure CDN with a Custom Domain</a></p>
