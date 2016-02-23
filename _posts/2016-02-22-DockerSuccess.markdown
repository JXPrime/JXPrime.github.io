---
layout: post
title:  "Jekyll and Docker Success"
date:   2016-02-22 22:20:00 -0700
categories: vagrant
---

Success!

Previously, I had mentioned my struggles trying to run the [Jekyll](https://hub.docker.com/r/jekyll/jekyll/) Docker container on my local machine. After some tinkering and reading, I've sorted it out.

On Windows, when you install Docker, what you're getting is a tiny little VM running Linux, and that VM is your Docker host. You administer that VM through the `docker-machine` comamnd. By default, your home folder (i.e., `c:\Users\Bob\') is accessible to that VM. I had my source code in a separate folder. After cloning my repository inside my home folder, I was able to run the command and see that the files were being served successfully.

This left the problem of connecting to the instance so I could view the result. Again, this is solved with the knowledge of the Docker VM. By connecting to the IP of that VM, and not to `localhost`, I was able to view the results successfully:

![Docker screenshot](/images/dockersuccess.png)