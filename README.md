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
```$ git clone git@github.com:lislis/middlemanghpages.git```

and cd into it  ```$ cd middlemanghpages```

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
