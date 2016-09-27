---
published: false
title: The Configuration API in .Net Core
layout: post
---
This is a good overview article on the Configuration system changes in .Net 5, or .Net Core 1.0 as it's being called now.

<a href="https://msdn.microsoft.com/en-us/magazine/mt632279.aspx"><img width="25%" src="https://msdn.microsoft.com/dynimg/IC842630.png" /><br/>https://msdn.microsoft.com/en-us/magazine/mt632279.aspx</a>

The key takeaways are:

The Configuration API is completely different to previous .net versions
You can still use your old config files to hold settings
You can capture and read Windows environment variables using the configuration API now
You can configure multiple sources to be read into the config "store" for an application. 
The last value read in for a given setting is the one that takes precedence, so you can easily override default settings.
LikeThe Configuration API in .Net Core