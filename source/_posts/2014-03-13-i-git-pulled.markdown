---
layout: post
title: "I git pulled"
date: 2014-03-13 21:20:56 -0500
comments: true
categories: [github, octopress, rake, blogging]
author: "Mr. Hyde"
---

I used the instuctions at `http://blog.zerosharp.com/clone-your-octopress-to-blog-from-two-places/`
to pull the source and master branches from GitHub:

```
$ cd octopress
$ git pull origin source  # update the local source branch
$ cd ._/deploy
$ git pull origin master  # update the local master branch
```

Then I ran `rake new_post' to create this post, after which I recreated the blog and pushed to master using

```
$ rake generate
$ rake deploy
```

Finally, I updated source using

```
$ git add -A              # update all changes including removed files
$ git commit -m "commit message"
$ git push origin source  # update the remote source branch"
```

As a reference, `https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet` has a nice cheatsheet for writing in Markdown.

