---
layout: default
title: "OpenShift Developer Notes"
date:   2017-01-09 10:55:59 +0000
categories: openshift developer notes redhat
tags: openshift developer notes docker redhat
---
# Red Hat OpenShift Developer Notes

## General Notes

- One way of looking at containers is as improved chroot jails
- Allow operating system (OS) process (or a process tree) to run isolated from other processes hosted by the same OS
- Each container gets an exclusive virtual network interface and private IP address
- Docker provides an easy CLI and API to create and manage containers
- Instead of issuing dozens of complicated commands to configure namespaces, cgroups, SELinux, and capabilities, Docker does that with a single easy-to-use command
- Docker also provides a standard container image format, which is actually a tar file (libraries, commands, and working derictories, plus metadata describing the image itself)
- Docker formatted container images, or simply container images, are immutable.
- Container images are layered:  A complex image can be built by stacking a base OS image under an app server image and then under app-specific binaries and libraries
- Docker formatted container images also provides a standard HTTP-based protocol for accessing image registires
- Image Registries are similar to yum / dnf / pacman repositories, but hosting container images instead of RPM package files.
- Any organization can host its own public or private registry for sharing container images

## Managing Containers with Docker Commands

- Docker runs as a system daemon that accepts requests through HTTP using a REST API
- To check if the Docker daemon is running, use **systemctl status docker**
- **docker images** - displays a list of Repository, Tag, Image ID, Created, Virtual Size
- **docker pull** - downloads images
- **image name syntax** - [registry_name/]**image_name**[:tag]
- **docker search** - search for images on known Red Hat container registries
- **docker load** - load an image from a tar file in the local files system to tht local Docker daemon
- **docker save** - save an image available from the local Docker daemon as a tar file in the local file system
- **docker rmi** - delete an image so it is no longer available from the local Docker daemon
- **docker tag** - add a tag to an image available from the local Docker daemon
- **docker run** - create a new container and start a process inside the new container

{% highlight bash %}
# docker run openshift/hello-openshift
{% endhighlight %}

- **docker ps** - list running containers
- **docker stop** - stop a running container
- **docker rm** - remove a stopped container, discarding its state a filesystem
- **docker logs** - show the container standard output.  It is expected that containerized applications send all their logs to standard output
- **docker exec** - start an additional process inside a running container
- **docker** - without any arguments, shows all docker commands and a brief description for each one

## OpenShift Enterprise by Red Hat Architecture

- OpenShift Enterprise is a set of microservices built over Red Hat Enterprise Linux, OSE adds PaaS capabilities over Atomic like remote management, multitenancy, increased security, application life-cycle management, and self-service interfaces for developers

![OpenShift Enterprise Software Stack]({{ site.baseurl}}/OpenShift_Software_Stack.svg){:class="img-responsive"}





