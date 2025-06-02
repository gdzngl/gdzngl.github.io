---
layout: post
title:  "Jekyll Quick Reference"
date:   2025-06-02 10:32:07 -0500
categories: howto 
tags: jekyll
description: A quick overview of the things I want to remember every time I come back to use jekyll and write a new post.
---

# Drafts

To create a draft make a new file in the _drafts directory with the following format:

`title.MARKUP`

# Formatting

All blog posts must begin with frontmatter.  The required data is `layout` and `title`.

{% highlight yaml %}
---
layout: post
title:  "Welcome to Jekyll!"
---
{% endhighlight %}

Code blocks like the YAML example above can be [created with the highlight tag](https://jekyllrb.com/docs/liquid/tags/#code-snippet-highlighting). The full list of languages can be found [here](https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers).


Images are stored under assets and right now I'm sorting them into folders by post month.

![code highlighting example](/assets/2025-06/code-highlighting-example.png)

# Posts

To create a post, move the file to your _posts directory with the following format:

`YYYY-MM-DD-title.MARKUP`

# About

Started from the [Chirpy Starter](https://github.com/cotes2021/chirpy-starter).
