---
layout: post
title: problem in Markdown with Jekyll
categories: markdown
description: some notes
keywords: markdown, jekyll
---

## Curly Braces in Markdown with Jekyll

Problem:
when using braces in Markdown with Jekyll, the braces and the contents inside the braces will not show.

Solution[^1]:

{% assign openTag = '{%' %}
{{ openTag }} raw %}

```cpp
{{ "{% raw " }}%} 
code block
{{ "{% endraw " }}%}
```

{{ openTag }} endraw %}

[^1]:<https://www.tomordonez.com/curly-braces-markdown-jekyll/>