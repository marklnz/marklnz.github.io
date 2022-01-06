---
published: false
title: Deploying .net core apps
tags: [.Net Core, Octopus Deploy, DevOps, CI/CD]
style: 
color: 
description: Using Octopus Deploy to facilitate CI/CD in DevOps, with .net core.
---
I use Octopus Deploy for all our team's release management needs currently, and I'm keen to do the same for our upcoming .Net Core projects. So when I read the article below from the team at Octopus, I was excited as it meant that they're looking at the issues involved, and have their finger on the pulse with regard to .net core. 

The article is a good guide to how things will work, but I have a few issues to sort out in my own team's case since we're using a slightly older version of .Net Core.  Also, as I've written about previously, we use Visual Studio Online Build to manage our CI builds, and this article talks about the situation if you're using TeamCity. 

But it's a useful read in any case, and I'd recommend it even if you're not using Octopus Deploy as it does touch on the publish/deploy commands that will be in the new .Net Core command line interface. 

<a href="https://octopus.com/blog/aspnet-core-build-and-deploy"><img width="33%" src="https://i.octopus.com/blog/201603-screenshot2016-03-09at11.08.29am-Z67T.png" /><br/>
https://octopus.com/blog/aspnet-core-build-and-deploy</a>