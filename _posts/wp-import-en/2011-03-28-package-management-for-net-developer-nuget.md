---
layout: post
title: "Package Management for .NET developer: NuGet"
date: 2011-03-28 10:28
author: CI Team
comments: true
categories: [Uncategorized]
tags: [NuGet]
language: en
---
{% include JB/setup %}


<p><a href="{{BASE_PATH}}/assets/wp-images-en/image145.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; margin: 0px 10px 0px 0px; padding-left: 0px; padding-right: 0px; display: inline; float: left; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" align="left" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb53.png" width="112" height="104" /></a>Those of you who are reading the <a href="http://haacked.com/">blog of Phil Haack</a> have properly heard something about NuGet. "Package Management" sounds a little bit bulky but if you are a developer you should take a look on NuGet - it pays <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-smile" alt="Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-smile8.png" /></p>  
  

<p><b>NuGet?</b></p>
<p><a href="http://nuget.codeplex.com/wikipage?title=Getting%20Started">NuGet</a> is an open source package management system which is developed from microsoftis and non-microsoftis (<a href="http://nuget.codeplex.com/wikipage?title=Getting%20Started">everything is open source</a>). It should work as a kind of contact point for every kind of open source libraries. It includes a wide filed from Javascript libraries, EMAH handler, NHibernate to Mocking Frameworks. Properly there are a lot more opportunities. </p>
<p><b>Okay cool ... but why?</b></p>
<p>It seems like this idea is born in the ASP.NET MVC team. In ASP.NET MVC it was the first time, that jQuery was included in the template. Of course this version will be old in a view days or weeks. Result: The developer is forced to collect the files by himself and look up for some updates. It´s the same thing with the server components like NHibernate. In the future NuGet will play an important deployment-role for many frameworks from Microsoft.</p>
<p><i></i></p>
<p><i>To say it short:</i></p>
<p><i>In fact NuGet works almost like the Extension Manager of Visual Studio 2010. There are several Microsoft Extensions as well....</i></p>
<p><b>If you are from the Ruby on Rails &amp; co. world</b></p>
<p>Yes... this already exists on several platforms. But anyway it´s nice and fits perfect into the Visual Studio Tool landscape. </p>
<p><b>Curious?</b></p>
<p><a href="http://www.hanselman.com/blog/NuGetActionPlanUpgradeTo11SetupAutomaticUpdatesGetNuGetPackageExplorer.aspx">- Scott Hanselman: NuGet Action Plan - Upgrade to 1.1, Setup Automatic Updates, Get NuGet Package Explorer</a></p>
<p><b>How does this look like in exercise?</b></p>  

<p>I´ve changed the jQuery library with the NuGet way on BizzBingo. The advantage is, that I´m now able to check up easily if there is a new version or not <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-smile" alt="Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-smile8.png" /></p>  

<p><a href="{{BASE_PATH}}/assets/wp-images-en/image146.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb54.png" width="504" height="260" /></a></p>
<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb387.png" width="363" height="270" /></p>
<p>You are able to download the Visual Studio doc files:</p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image147.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb55.png" width="276" height="253" /></a></p>
<p>The files are loading into the Script directory - but you have to referent them by yourself. In the project a "package.config" file will be created:</p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image148.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; margin: 0px 10px 0px 0px; padding-left: 0px; padding-right: 0px; display: inline; float: left; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" align="left" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb56.png" width="146" height="272" /></a>Here it´s written which package is installed and which version. The packages will be saved nearly the SLN files in an extra directory so you are able to save all the files in the version administration. </p>
<p>If you start your application there is no Voodoo or dark magic happening. NuGet is down loading the files as packages an copy them into the project. Depending on the package there will be some changings of the web.config. But there is nothing bad happening while it runs.</p>  

<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb390.png" width="394" height="248" /><b></b></p>
<p><b>Where did I get NuGet? What kinds of Packages are existing?</b></p>
<p>On the <a href="http://nuget.org/List/Packages">NuGet gallery</a> you can take a look on the actual packages:</p>
<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb391.png" width="422" height="314" /></p>
<p>NuGet is a relatively "young" program - but there is a daily growing community using this service. Of course there are some packages missing but everyone is able to upload new <img style="border-bottom-style: none; border-right-style: none; border-top-style: none; border-left-style: none" class="wlEmoticon wlEmoticon-smile" alt="Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-smile8.png" /></p>
<p>For friends of statistics: <a href="http://stats.nuget.org/">stats.nuget.org</a></p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image149.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-en/image_thumb57.png" width="417" height="353" /></a></p>
<p>You can take a look on "<a href="http://nuget.codeplex.com/wikipage?title=Getting%20Started">Getting Started</a>" on Codeplex. At the front page of <a href="http://nuget.org/">nuget.org</a> you will find the link to the installer of Visual Studio. </p>
