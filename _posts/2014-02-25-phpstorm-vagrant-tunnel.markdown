---
layout: post
title: "Debugging and testing over PHPStorm – SSH – Vagrant tunnel"
date: 2014-02-25
owner: Chris
tags: [vagrant,phpstorm,ssh,php,testing,debugging]
---

We are happy to publish a handy [Vagrant](http://www.vagrantup.com/) plugin which makes debugging and testing easy
if you use [PhpStorm](http://www.jetbrains.com/phpstorm/) and Vagrant box.
The main idea is to add concept of debugging over SSH tunnel. Currently only HTTP concept is supported by default
so this is a workaround for a missing feature in PhpStorm (see [here](http://youtrack.jetbrains.com/issue/WI-19485)).

<!--more-->

### What it does?
`vagrant-phpstorm-tunnel` installs a proxy php binary which can be configured as a php-interpreter in PhpStorm.
It will forward all php calls to `php` in the Vagrant VM.

### Why SSH?

- running non WEB based application in the box
- executing php code in the box
- unit testing
- debugging

### Installation
{% highlight ruby %}
vagrant plugin install vagrant-phpstorm-tunnel
{% endhighlight %}

More information on [Github](https://github.com/cargomedia/vagrant-phpstorm-tunnel)
