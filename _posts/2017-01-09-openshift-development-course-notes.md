---
layout: default
title: "OpenShift Developer Notes"
date:   2017-01-09 10:55:59 +0000
categories: openshift developer notes
tages: openshift developer notes docker
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
