---
toc: true
comments: true
layout: post
title: GitHub Pages
description: Build your first Blog.  This will help us communicate results.
type: plans
courses: { csse: {week: 1}, csp: {week: 1, categories: [4.A]}, csa: {week: 0} }
categories: [C1.4]
---
# 
With all of this in place, we can spin up the development container inside VS Code. Then, from the VS Code terminal in our Docker container environment, we can run docker-compose up in the root of our project. This will start up our individual service containers on the host machine. But, thanks to the shared network and volumes, we can continue to edit code in our development container and see the changes immediately show up on our services!

It’s also possible to use the Docker CLI to shut down or restart services as needed in development. You can even open another VS Code window and use the Remote-Containers extension to connect to one of the running service containers to directly inspect logs, edit code within that constrained environment, etc. This is a generic setup that can work for any project. Onboarding new developers requires just installing VS Code and Docker and then cloning the repository and opening it in a container. The initial setup is a lot of work, but I think this is the cleanest development experience you can get with Docker right now.
