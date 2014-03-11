middlemanghpages
================

A Middleman setup with blogging functionality and deployment options to gh-pages.  
Plugins used:
  * [Middleman Livereload](http://middlemanapp.com/basics/livereload/)
  * [Middleman Blog](http://middlemanapp.com/basics/blogging/)
  * [Middleman Deploy](https://github.com/middleman/middleman-blog)
  * [Middleman Favicon Maker](https://github.com/follmann/middleman-favicon-maker)

## Setup

Clone the repo
```$ git clone git@github.com:rails-girls-summer-of-code/summer-of-code.git```

and cd into it  ```$ cd summer-of-code```

Install the dependencies  ```$ bundle install```  

## Develop

```$ middleman```
will start a server on port :4567.  
It comes with live reload and compiles scss to css  
and markdown (only in blogposts) to html on the fly.

## Deploy
```$ middleman deploy```
will automatically run  ```$ middleman build``` first (so you don't have to)  
and after that deploys the build
to the gh-pages branch of the remote repository.

## Edit Content

### Pages

Everything you need is in the /source folder. Create a new page with the suffix .html.erb in /source or a subfolder (e.g. /source/students). That will also be the url (e.g. the file /source/something.html.erb will be /something/ later).  
In Pages you can write html and use everything else you cn use in erb templates.

### Blog

In the folder /source/blog/ the individual blogposts are stored. Those files can be markdown files. The naming convention for a blogpost ist year-moth-day-title.md

### Frontmatter

Frontmatter is the little block of variables called the beginning of each page.
for usual pages ```title``` is the only one defined. Blogposts have more options:  
```
---
title: Some title
date: 2014-02-24
tags: sometag
author: Some Author
twitter: someone
---
```
Title is used for the title tag in the head. Date is optional and cann overwrite the date in the filename. Tags (comma seperated) are used for tags. Author and twitter are custom and referenced in the layout.

### Layout and styles

There are two layouts, one for pages and one for posts. You can add more in /source/layouts and then use frontmatter to apply it.  
Includes are stored in modules. Add more as neccessary.  
Styles are written in scss. Don't worry, it is completely compatible with css syntax. So if you don't care then throw your styles into /source/styles/gui/_layout.scss and everything will be fine.  

To format pages you need the following markup
```
<!-- .inner centers the content -->
<div class="inner">
  <!-- .content is for the big column -->
  <div class="content"></div>
  <!-- .sidebar is for the small column -->
  <div class="sidebar"></div>
  <!-- .fullwidth uses the full width of the centered content -->
  <div class="fullwidth"></div>
</div>
```

You can also check what's already there and adjust your markup.

