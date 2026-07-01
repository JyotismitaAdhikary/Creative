---
layout: post
title: "A weekend with watercolours"
date: 2026-06-28
tags: [painting]
---

Spent Sunday afternoon on a small watercolour study. Still figuring out how much
water is *too* much water — apparently quite a lot less than I think.

Here's how you embed an image inside a post (the file lives in `assets/images/`):

![A watercolour study]({{ "/assets/images/painting1.jpg" | relative_url }})

That `{% raw %}{{ "..." | relative_url }}{% endraw %}` bit just makes sure the
link works whether the site is hosted at the root or in a sub-folder. Copy that
pattern any time you add an image to a post.
