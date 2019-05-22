---
id: 2256
title: Atom Python Setup
date: 2015-11-12T16:23:35-05:00
author: Tim Schnell
layout: post
guid: http://tims.io/?p=2256
permalink: /atom-python-setup/
dsq_thread_id:
  - "4313719271"
image: /wp-content/uploads/2015/11/atom.jpg
categories:
  - Code
  - Python
tags:
  - atom
  - Python
---
## Install Atom

<a href="https://atom.io" target="_blank" rel="noopener">https://atom.io/</a>

## Install Python Linter

Atom -> Preferences -> Install

<a href="https://atom.io/packages/linter-flake8" target="_blank" rel="noopener">https://atom.io/packages/linter-flake8</a>

If you have trouble getting the linter to be on your pythonpath:

Add this to your init script: Atom -> Open Your Init Script

<pre class="lang:default decode:true">process.env.PATH = ['/usr/local/bin/', process.env.PATH].join(':')</pre>

I also don&#8217;t want the linter to freak out every time a line is longer than 80 characters so I ended up adding this to my config file.

<pre class="lang:default decode:true">"linter-flake8":
  maxLineLength: 120
  maxComplexity: 20

editor:
 preferredLineLength: 120</pre>

&nbsp;

## Update Settings

Atom -> Preferences -> Settings

  * Make sure Soft Tabs is checked
  * Tab Length should be set to 4 (default is 2)

&nbsp;