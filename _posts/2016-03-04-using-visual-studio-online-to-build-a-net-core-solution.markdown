---
published: true
title: Using Visual Studio Online to build a .net core solution
layout: post
---
# The situation

I've been working recently on some .net core projects, and the time has come to set up a proper build and deploy process for them. Development of business functionality that will require system testing is about to begin, and in order to get into the groove of code-unit test-deploy-test-release cycle as quickly as possible, I need a repeatable automated process in place.

# The tools

For the projects we currently have in production, which are all based on earlier versions of .net (mostly 4.0) across the whole stack, we have an instance of Visual Studio Online set up. We use Git repositories for version control, and we currently use Octopus Deploy for release management and deployment. 

The current process is that each developer will build and unit test their code on their local machine, and commit to their local git repository, before then pushing their branch up to the server, and creating a pull request. Once the pull request is approved, their code is merged to the Master branch, and a Continuous Integration build is run. This builds the code, runs the build verification tests, packages and creates a release in Octopus Deploy, and deploys the release to the first of our test environments. That process needs to remain the same. 

# Building "old" .net

With the "old" .net framework, the Visual Studio Online Build process is simple to configure - I have a "set version number" script that I run first off to synchronise the version number across all the built assemblies, as I like to like the version number to the build by incorporating it into the assemblyinfo for each project. Apart from that, the rest is just a "Visual Studio build" step, a "Visual Studio Test" step, then an Octopus Deploy step to upload the packaged build artifacts to the deployment server and deploy them.

# Building .net Core

Unfortunately it's not QUITE that simple for .net core. At least, not yet. I found that you can't rely on the Visual Studio Build and Test steps to do the heavy lifting. Instead, I've written some powershell scripts to do the equivalent. 

So my process now looks like this:

* Powershell task (to run the Tests)
* Publish test results task
* Powershell task (to Publish the deployable components)

The key things to note are that

1. There is no build
1. Tests are run BEFORE the packaging
1. No visual studio tasks anywhere
1. You definitely need to learn the various DNVM and DNU command line options, plus know how to use DNX to run the commands defined in a project.json file. 

This is still a work in progress, and I'll likely consider redoing it all again once .net core reaches RTM. The command line interfaces are changing, and by RTM, the Visual Studio Build tasks will likely include support for .net core. 

Next step for me: get the build integrated with our deployment tool!