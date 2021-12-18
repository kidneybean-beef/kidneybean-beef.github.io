---
layout: post
title: Blog Establishment
categories: learnToBlog
description: some notes when establishing this blog
keywords: keyword1, keyword2
---

## How I build this

First I forked this blog template from 
Zhuang Ma
https://mazhuang.org/.

Besides this, I met a problem when I edited something, and pushed to git, an error message occurred on github->Actions:
`The deploy step encountered an error:The process '/usr/bin/git' failed with exit code 128`

The solution is adding this

```yaml

GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```

in the last part of file: .github/workflows/ci.yml[^1].


[^1]:<https://hbuecx.com/post/github-action-gou-jian-shi-bai-chu-li/>