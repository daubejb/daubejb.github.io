---
layout: default
title:  "Test Driven Development with Python"
date:   2017-01-13 14:17:59 +0000
categories: notes development
tags: notes development learning python selenium django testdrivendevelopment
---
# Test Driven Development with Python

by Harry Percival


> Functional tests should help you build an applicaiton with the right functionality, and guarantee you never
> accidentally break it.  Unit tests should help you to write code that's clean and bug free.

## Setting up the virtualenv

1. **Install** virtualenv

{% highlight bash linenos %}
pip install --user virtualenvwrapper
echo "source virtualenvwrapper.sh" >> ~/.bashrc
source ~/.bashrc
{% endhighlight %}

2. **Create** a virtualenv *called environment-name*

{% highlight bash %}
mkvirtualenv --python=python3 environment-name
{% endhighlight %}

3. **Activate** the environment

{% highlight bash %}
workon super lists
{% endhighlight %}

4. **Check** which Python

{% highlight bash linenos %}
which python
python --version
{% endhighlight %}

5. **Install** Django and Selenium

{% highlight bash %}
pip install "django<1.11" "selenium<3"
{% endhighlight %}



