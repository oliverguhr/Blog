---
layout: post
title: "Glimpse Web Debugging: Firebug for the Server side"
date: 2011-04-17 16:13
author: CI Team
comments: true
categories: [HowTo]
tags: [Glimpse, NuGet]
language: en
---
{% include JB/setup %}

  

<p><a href="{{BASE_PATH}}/assets/wp-images-en/image155.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; margin: 0px 10px 0px 0px; padding-left: 0px; padding-right: 0px; display: inline; float: left; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" align="left" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb63.png" width="81" height="80" /></a>How do I get to know what´s happening inside a web application without a lot of logging or to stop with the debugger everywhere? Today I was introduced to a nice helper: <a href="http://getglimpse.com/">Glimpse</a> - it works almost similar to firebug but it analyzes the server side <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-smile" alt="Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-smile10.png" /></p>  
  

<p><b>What is Glimpse able to do?</b></p>  

<p>With a little Widget what you can find in the web interface you get to know which Session variables are set, which route was taken, which view, which Action/Filter is called and so on. </p>  

<p>In the Moment it works for ASP.NT MVC and ASP-NET WebForms. </p>
<p><u>Be careful: </u>It seems like there are some bugs left at the moment. For BizzBingo the try to show it on the front page failed because the Module destroys something - but the version is at 0.76 beta at the moment <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-winkingsmile" alt="Zwinkerndes Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-winkingsmile19.png" /></p>
<p>Here you can see a little video the developers have made:</p>  
  <div style="padding-bottom: 0px; margin: 0px; padding-left: 0px; padding-right: 0px; display: inline; float: none; padding-top: 0px" id="scid:5737277B-5D6D-4f48-ABFC-DD9C333F4C5D:8d686b5d-6c0f-4a77-8ff9-2cbceef0200b" class="wlWriterEditableSmartContent"><div><object width="448" height="252"><param name="movie" value="http://www.youtube.com/v/ke8Rw2BGPG0?hl=en&amp;hd=1"></param><embed src="http://www.youtube.com/v/ke8Rw2BGPG0?hl=en&amp;hd=1" type="application/x-shockwave-flash" width="448" height="252"></embed></object></div></div>
<p><b>Installation - NuGet!</b></p>
<p>The installation is very easy over NuGet:</p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image156.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb64.png" width="506" height="131" /></a></p>
<p><b>Configuration</b></p>  

<p>Now you have to start glimpse: </p>
<p>On <a href="http://www.yoursite.com/Glimpse/Config">http://www.yoursite.com/Glimpse/Config</a> or <a href="http://localhost/Glimpse/Configdev">http://localhost/Glimpse/Config</a> just turn the Module "on". </p>
<p><b>That´s it</b></p>
<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb429.png" width="513" height="227" /></p>  

<p>Everything else you will find on <a href="http://nuget.org/List/Packages/Glimpse">NuGet</a> or <a href="http://getglimpse.com/">http://getglimpse.com/</a></p>
