---
layout: post
title: "Octopress Basics Recap"
date: 2014-04-08 06:43:14 -0700
comments: true
categories: [octopress, tutorials, markdown]
---
```bash Octopress Cheatsheet
# create a new post
rake new_post['Title of the post']

# create a new page
rake new_page['Title of the page']

# preview your work
rake preview

# publish it
rake generate && rake deploy

# commit and backup(automatic message)
git commit -am "`date`" && git push origin source
```