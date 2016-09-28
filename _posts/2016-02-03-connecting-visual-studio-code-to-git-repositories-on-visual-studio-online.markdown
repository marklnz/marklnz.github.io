---
published: true
title: Connecting Visual Studio Code to git repositories on Visual Studio Online
layout: post
---
I recently had a problem with Visual Studio Code that had me nearly tearing my hair out. 

VS Code has built in support for git version control, so naturally you'd assume that VS Code would support git repositories that are hosted on Visual Studio Online. However I just could not get VS Code to authenticate to Visual Studio Online when I wanted to pull changes down from the repo I was using. 

Using the git command line worked, and using GitHub Desktop also worked, but I believe that it's best to use the built in tool wherever possible, to reduce the productivity hit you get from switching tools for different, but related, tasks. So I REALLY wanted to work out how to get this working from within VS Code. 

Turns out it's pretty easy actually - I found a tool called the Git Credential Manager for Windows, which Microsoft built to provide better support for git logins to VS Online. 


<a href="https://github.com/Microsoft/Git-Credential-Manager-for-Windows"><img width="33%" src="https://avatars0.githubusercontent.com/u/6154722?v=3&s=400" /><br/>https://github.com/Microsoft/Git-Credential-Manager-for-Windows</a>


Basically you just install this, and it registers with git as a credential manager, and you're away. Next time you log into a VS Online-hosted repository using git (e.g. when doing a git pull from the command line), you are presented with a familiar looking logon page. You just enter your VS Online credentials and you're away. 

Because VS Code uses the git tools under the covers, this naturally covers VS Code as well. In fact there are plenty of code editors that also do this, so you're covered with those other tools also.

With VS Online, one of the more painful things with authentication is that you generally can't log on from client tools using the Microsoft Account credentials that you'd usually use. Most client tools don't know how to initiate and manage an OAuth flow to achieve this.

To get around this limitation, VS Online supports non-OAuth connections using a set of alternative credentials or access tokens that you can set up. Both of these are painful however, as you have to configure and manage them separately, remember or write down the credentials, etc., etc.

However, the Git Credential Manager tool allows you to use your regular Microsoft Account credentials to log in, as it takes care of the OAuth stuff for you. 

And, best of all, this is an open source tool. Hosted on GitHub. Built by Microsoft. Yep, this is definitely not the Microsoft of old!! 