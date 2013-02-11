---
layout: post
title: Creating this page
category : development
tags : [development, jekyll, tutorial, foundation]
---
{% include JB/setup %}

As a first post I want to outline how I created this page to help other people with the creation of their new page.

## Overview 

### What is Jekyll?

Jekyll is a parsing engine bundled as a ruby gem used to build static websites from
dynamic components such as templates, partials, liquid code, markdown, etc. Jekyll is known as "a simple, blog aware, static site generator".

### Examples

This website is created with Jekyll. [Other Jekyll websites](https://github.com/mojombo/jekyll/wiki/Sites).



### What does Jekyll Do?

Jekyll is a ruby gem you install on your local system.
Once there you can call `jekyll --server` on a directory and provided that directory
is setup in a way jekyll expects, it will do magic stuff like parse markdown/textile files, 
compute categories, tags, permalinks, and construct your pages from layout templates and partials.

Once parsed, Jekyll stores the result in a self-contained static `_site` folder.
The intention here is that you can serve all contents in this folder statically from a plain static web-server.

You can think of Jekyll as a normalish dynamic blog but rather than parsing content, templates, and tags
on each request, Jekyll does this once _beforehand_ and caches the _entire website_ in a folder for serving statically.

### Jekyll is Not Blogging Software

**Jekyll is a parsing engine.**

### The Jekyll Application Base Format

Jekyll expects your website directory to be laid out like so:

    .
    |-- _config.yml
    |-- _includes
    |-- _layouts
    |   |-- default.html
    |   |-- post.html
    |-- _posts
    |   |-- 20011-10-25-open-source-is-good.markdown
    |   |-- 20011-04-26-hello-world.markdown
    |-- _site
    |-- index.html
    |-- assets
        |-- css
            |-- style.css
        |-- javascripts


- **\_config.yml**  
	Stores configuration data.

- **\_includes**  
	This folder is for partial views.

- **\_layouts**   
	This folder is for the main templates your content will be inserted into.
	You can have different layouts for different pages or page sections.

- **\_posts**  
	This folder contains your dynamic content/posts.
	the naming format is required to be `@YEAR-MONTH-DATE-title.MARKUP@`.

- **\_site**  
	This is where the generated site will be placed once Jekyll is done transforming it. 

- **assets**  
	This folder is not part of the standard jekyll structure.
	The assets folder represents _any generic_ folder you happen to create in your root directory.
	Directories and files not properly formatted for jekyll will be left untouched for you to serve normally.

(read more: <https://github.com/mojombo/jekyll/wiki/Usage>)


