---
title: "Install Jekyll and Run"

categories:
  - Blog
tags:
  - jekyll
  - ruby
last_modified_at: 2020-08-21T12:32:00-0700
---

1.Install Ruby first

```
brew install ruby
```

then add ruby path to .bashrc or .zshrc

2.Install Jekyll and bundler as well

```
gem install -n /usr/local/bin jekyll bundler
```

3.Create a page and run to check

```
jekyll new helloBlog

cd helloBlog

bundle exec jekyll serve
```

then go to the preview address in the browser.
