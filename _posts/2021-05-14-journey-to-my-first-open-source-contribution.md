---
layout: post
title: "Journey to my first open source contribution"
date: 2021-05-14 11:52:00
categories:
---

Recently I was able to make my first contribution to an open source project [nbstripout](https://github.com/kynan/nbstripout/).
Contributing to an open source project has been a dream of mine since I was introduced to the idea of open source during my undergrad.
In this post, I am sharing my attempts to contribute to the open source community and lessons learned along the way.

### My introduction to Open Source
![Ubuntu Logo](https://upload.wikimedia.org/wikipedia/commons/1/16/Ubuntu_and_Ubuntu_Server_Icon.png)

*Canonical Ltd, CC BY-SA 4.0 <https://creativecommons.org/licenses/by-sa/4.0>, via Wikimedia Commons*

I remember after the third semester (2009) of my undergrad at Vivesvaraya National Institute of Technology a few of my seniors introduced our class to Ubuntu.
They showed a lot of cool features like wiggly windows, multiple workspaces, system customization, and many more.
Since the beginning when I was using mostly Windows-based computers I always felt I had very little control over the system.
All the things had to be done a certain way as Microsoft intended.
Seeing the level of control available in Linux based systems like Ubuntu felt quite liberating.
And the idea of using the command line to do everything especially installing software made me fall in love with Ubuntu and eventually the overall Linux ecosystem.
As I started using Ubuntu regularly, I wanted to contribute to the open source community.

### Attempts in contribution to open source
#### The Linux Kernel
In most introductions to open source, the success of Linux kernel development as an open source project is celebrated.
And rightly it should be.
Naturally, I felt the need to contribute to the Linux kernel itself to make my contribution worthwhile.
But then reality struck.
The Linux kernel is a giant beast and I was a simpleton undergrad who just started learning to program.
In those days getting Linux kernel source code to compile was itself an achievement especially for a newbie to programming like me.
On top of that, the Linux kernel map looks like this.

![Linux Kernel Architecture](https://upload.wikimedia.org/wikipedia/commons/5/5b/Linux_kernel_map.png)
*Conan at English Wikipedia, CC BY 3.0 <https://creativecommons.org/licenses/by/3.0>, via Wikimedia Commons*

Daunting right? I did not even know where to start contributing.
I did not know about LKML.
Github was yet to be a thing. At least in India.
So I had no idea where to contribute at all.

#### Evince PDF Reader
![Evince](https://upload.wikimedia.org/wikipedia/commons/9/9b/GNOME_Document_Viewer_icon_2019.svg)

*https://gitlab.gnome.org/jimmac, GPLv2 <https://www.gnu.org/licenses/old-licenses/gpl-2.0.html>, via Wikimedia Commons*

As a full-time Linux user, I was doing everything on my Ubuntu system.
For reading PDFs I was using Evince PDF reader.
 I always felt the need to annotate PDF documents to keep digital copies of my notes and not worry about losing them ever.
So then I downloaded the source code for Evince PDF reader.
But I had no idea about PDF files.
How do they work? How to introduce the annotation feature?
There was very little information available online about the PDF files at the time.
I did not know that what build tools are.

### My own source project
When I started working in the industry, I got introduced to SDLC, SOLID design principles, build tools, design patterns, CI, CD, and much more.
It was quite exciting.
While working on our project, we were configuring the same application for different environments like DEV, QA, STG and, PROD.
There was a separate config file for each environment.
I observed that many configs were the same across those environments.
I developed a small Gradle plugin with which the common configs were in a default config file.
And environment-specific configs would be mentioned only when they had a different value other than the default value.
I published this plugin to Bintray as well.
It did not take off as I did not do any publicity.
However, I felt good that I was able to share my idea with the world.

### My recent contribution to `nbstripout`
In one of my recent projects, I was working with the Apache Spark framework.
My work involved a lot of exploration of data and Apache Zeppelin notebooks make this quite easy with its UI.
When I felt the need to check in the zeppelin notebooks I had written due to the mechanism of storage of zeppelin notebooks it also embeds the output of queries I have written which makes them unsuitable to check into Git.
I had to manually clear the output each time I had to check in a version of the notebooks I was writing.
I thought surely someone else might have solved the problem.
But I could find no project which made it easy to version control zeppelin notebooks.
I knew Zeppelin notebooks were similar to Jupyter notebooks since I had previous experience with Jupyter notebooks.
I found `nbstripout` which did exactly what I was looking for but that project was only handling Jupyter notebooks.
And here was my opportunity to contribute to an open source project once more.
I created a Github issue, had a good discussion with the maintainer of the repo.
Made changes as required and voila my pull request got merged into the mainline.
You can check my pull request [here](https://github.com/kynan/nbstripout/pull/130).

<center><img src="/img/honest_work.jpeg" alt="Honest Work Meme" width="500"/></center>
### Lessons learned
* Just because the introduction to open source happens by an example of Linux kernel it does not mean you only have that single open source project for contribution.
There are many open source projects that you can contribute to.
I am not discouraging anyone to contribute to the Linux kernel.
Learn about Linux kernel and contribute. Power to you.
* Take time to learn the source code and architecture of the project you wish to contribute to.
Build enough knowledge so that you know where and how to make changes.
How to test them. And how to get them to the mainline.
* If you start your open source project make sure you promote it.
Give talks about it at your local events.
Build a community around it.
It will fuel more ideas and will enhance your project or even start new projects.
Please don't get hung up on the fact that your current project will be dead.
We all are a part of the open source community.
Your project did its part by sparking new ideas.
Have the passion to execute your as well as other’s ideas.
Let's build great things together.
* Keep an eye out for improvements in the open source software you are using.
Which features you would like.
And pitch those features to the maintainers of the project.
Once the feature is approved do your best to implement and contribute.
All the best.
<center><img src="/img/open_source.jpeg" alt="Open Source Meme" width="500"/></center>
