---
layout: post
title: problem in Markdown with Jekyll
categories: markdown
description: some notes
keywords: markdown, jekyll
---

## Curly Braces in Markdown with Jekyll

Problem:

1. when using braces in Markdown with Jekyll, the braces and the contents inside the braces will not show.

   Solution[^1]:
Enclose the code block in raw and endraw tags.

```cpp
{% raw %}{%{% endraw %} raw %}
code block
{% raw %}{%{% endraw %} endraw %}
```


2. when using {% raw %} in a code block inside {% raw %}, this md can not be built by Jekyll.

   Solution[^2]:
Put the first {% inside a raw tag, so escaping it avoids the rest being processed:

```cpp
{% raw %}{%{% endraw %} endraw %} raw %}
code block
{% raw %}{%{% endraw %} raw %}{% raw %}{%{% endraw %}{% raw %}{%{% endraw %} endraw %} endraw %}
```

[^1]: <https://www.tomordonez.com/curly-braces-markdown-jekyll/>
[^2]: <https://stackoverflow.com/questions/47106191/how-to-display-raw-and-endraw-using-markdown>