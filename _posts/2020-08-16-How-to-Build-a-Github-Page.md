---
layout: post
title: How to Build a Github Page
category: Jekyll
tag: create-blog
---

Refer to wklchris's blog to build the Github Page based on Jekyll.
After building the Github Page, blogs can be written using Markdown.

<!-- more -->

## Install Ruby and dev-kit 

Go to [Ruby Site](http://rubyinstaller.org/downloads/) to download and install Ruby with Development Kit, For example rubyinstaller-devkit-2.6.6-1-x64. 

## Install Jekyll and Bundle


```
cmd cd C:\\Ruby26-x64
gem install jekyll
gem install bundle
```

## Blog Folders Initialization

Create following new folders in username.github.io：

- \_includes 
- \_layouts create a file: default.html (blank)
- \_posts 
- \_site 

Create a file:
- \_config.yml , content：  

```
title: Sherry' blog
author: Sherry
email: Sherry AT hotmail DOT com
description: > # this means to ignore newlines until "baseurl:"

baseurl: ""
github_username:  sherry725

defaults:
  -
    scope:
      path: "posts" #Indicate foler of posts 
    values:
      layout: "default"
      theme: minima


# Build settings
permalink: /:title.html
excerpt_separator: "<!-- more -->"

```

Create another file
- index.md, content：

```
layout: home
```

Create another file with type of File (no any .xxx)
- Gemfile 

```
# frozen_string_literal: true

source "https://rubygems.org"

gem "minima"

# gem "rails"
```

## Write Blogs

Create a Markdown file in folder of _posts, name of the file is like：

    1900-01-01-this-is-the-title.md

Add following heading：

```
---
layout: post
title: How to Build a Github Page
category: Jekyll
tag: create-blog
---
```

If you don't change the parmalink property at the heading，then the website of the blog is：

    username.github.io/this-is-the-title.html

## Test before publishing

cmd cd username.github.io
```
bundle install
bundle exec jekyll serve
```

if you edit \_config.yml, you need to execute the first line; otherwise you just need to execute the second line.

Now you can preview your blog through [http://127.0.0.1:4000](http://127.0.0.1:4000).

If you don't want to preview, just execute `jekyll build` and push through git.

## Others
[My Github Repository](https://github.com/sherry725/sherry725.github.io)
