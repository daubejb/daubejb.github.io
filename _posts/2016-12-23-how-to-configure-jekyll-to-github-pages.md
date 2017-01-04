---
layout: default
title:  How to configure Jekyll to GitHub Pages on Arch Linux
date:  2016-12-23 08:33:45 +0000
categories: howto
tags: howto githubpages archlinux jekyl
---
# How to configure Jekyll to GitHub Pages on Arch Linux

## Introduction
I am constantly learning new things and wanted a place to openly take notes locally on my laptop and have them automatically back up to the public Internet.  After some research, I landed on my existing Google domain [jeffdaube.com](http://jeffdaube.com), [Github Pages](https://pages.github.com/), and [Jekyll](https://jekyllrb.com/).

## Install Jekyll

In Terminal:
{% highlight bash %}
1 pacman -S ruby
2 gem update
3 gem install jekyll
4 jekyll new *your-site-name*
{% endhighlight %}
The generated Jekyll directory will look like:

Insert image here

## Run the site

1. $ bundle exec jekyll serve --watch
2. **open** http://localhost:4000 in an Internet browser
3. any **changes** made to the site will trigger a re-build

## Create Github Pages repository

1. **Login** to Github.com
2. **Create** a new repository with *username.github.io*
3. **Click** *Clone or download*
4. **Copy** the *Clone to HTTPS* link to clipboard

## Connect Local Jekyll site to Github

1. **Navigate** to the previously created *your-site-name* directory
In Terminal:
```bash
2 git init
3 git add --all
4 git commit -m "First commit"
5 git remote add origin https://github.com/username/username.github.io.git
6 git checkout master
7 git log origin/master
8 git merge origin/master
9 git push -u origin master (enter your user name and password for Github)
```
