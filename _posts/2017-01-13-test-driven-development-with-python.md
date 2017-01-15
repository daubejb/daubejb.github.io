---
layout: default
title:  "Test Driven Development with Python"
date:   2017-01-13 14:17:59 +0000
categories: notes development
tags: notes development learning python selenium django testdrivendevelopment
---
# Test Driven Development with Python

My notes from reading the book [Test Driven Development with Python](http://www.obeythetestinggoat.com/pages/book.html)

by Harry Percival


> Functional tests should help you build an applicaiton with the right functionality, and guarantee you never
> accidentally break it.  Unit tests should help you to write code that's clean and bug free.

## Setting up the virtualenv

### **Install** virtualenv

{% highlight bash linenos %}
pip install --user virtualenvwrapper
echo "source virtualenvwrapper.sh" >> ~/.bashrc
source ~/.bashrc
{% endhighlight %}

### **Create** a virtualenv *called environment-name*

{% highlight bash %}
mkvirtualenv --python=python3 environment-name
{% endhighlight %}

### **Activate** the environment

{% highlight bash %}
workon environment-name
{% endhighlight %}
  - to deactivate, $ deactivate

### **Check** which Python

{% highlight bash linenos %}
which python
python --version
{% endhighlight %}

### **Install** Django and Selenium

{% highlight bash %}
pip install "django<1.11" "selenium<3"
{% endhighlight %}

### Get Django Up and Running

- **Create** Project and Start Server

{% highlight bash linenos %}
django-admin.py startproject project-name
cd project-name
python manage.py runserver
{% endhighlight %}

### **Start** a Git Repository

{% highlight bash linenos %}
cd project-name
git init .
echo "db.sqlite3" >> .gitignore
echo "__pycache__" >> .gitignore
echo "\*.pyc" >> .gitignore
git status
git add --all
git commit -a
{% endhighlight %}

### **Create** an Application
{% highlight bash linenos %}
cd project-name
python manage.py startapp app-name
{% endhighlight %}

### **Create** a Unit Test
{% highlight bash linenos %}
vim app-name/tests.py
{% endhighlight %}

## Django's MVC, URLs and View Functions

Django's main job is to do something when a user asks for a URL.  Django's workflow:

1. HTTP *request* comes in for a URL
2. Django's rules decide which *view* function handles the request (*resolving* the URL)
3. View function processes the request and returns an HTTP *response*

### urls.py

Django uses a file *urls.py* to define how URLs map to view functions --- located in project-name/project-name folder

- **Add** url(r'^$', views.home_page, name='home'); to urls.py

## Useful Commands and Concepts

### Run the Django dev server
{% highlight bash %}
python manage.py runserver
{% endhighlight %}

### Run the functional tests
{% highlight bash %}
python functional_tests.py
{% endhighlight %}

### Running the unit tests
{% highlight bash %}
python manage.py test
{% endhighlight %}

### The unit-test/code cycle

1. Run the unit tests in the terminal.
2. Make a minimal code change in the editor.
3. Repeat!

### Don't Test Constants Rule, and Templates

Unit tests are about testing logic, flow control, and configuration

Templates are a very powerful feature of Django.  Strength consists of substituting Python variables
HTML text

Django requires all applications to be registered within the INSTALLED_APPS definition inside settings.py

## TDD Process

![TDD Process]({{ site.baseurl}}/TDD_process_with_functional_and_unit_tests.png){:class="img-responsive"}


