---
title: "github.io Pages"
excert: "It's been 3 years that I did not update the page 😁"

categories:
  - Blog
tags:
  - blog
last_modified_at: 2020-08-20T10:32:00-0700
---

GitHub Pages are public web hosted for free through GitHub. GitHub users can create and host both personal websites and websites related to specific GitHub projects. Pages lets you do the same things as GitHub, but if the repository is named a certain way and files inside it are HTML or Markdown.

It can be used like a Javascript template that is "\{\{ \}\}", for example, this post title is "{{ page.title }}" and last updated date is {{ page.last_modified_at }}.

```html
{ { page.title } }
```

```
{ { page.last_modified_at } }
```

### Image post test

#### MD format

![2008 Mini Cooper S](/assets/images/2020-08-20 17.22.07_PS5TGq.png){:class="img-responsive"}

#### HTML figure

<figure>
  <img src='{{ "/assets/images/2020-08-20 17.22.07_PS5TGq.png" | relative_url }}' alt='2008 Mini Cooper S' class='img-responsive'>
  <figcaption>2008 Mini Cooper S</figcaption>
</figure>
