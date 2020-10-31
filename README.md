# Hugo Theme Wiki

**A simple and beautiful Hugo theme based on GitHub's Primer CSS** 

This is the theme for my personal tech wiki!

Try it now, and leave me a star if you like it!

## Features

- [x] Github Like CSS
- [x] Menu Bar
- [x] Colored Code Pen
- [x] Math Inline
- [x] TOC Support
- [x] TimeLine
- [x] Tags & Categories
- [x] Social Share Buttons
- [x] Font Awesome Icons
- [x] Code Copy Button 


## Installation

Clone to your theme directory:

```terminal
git clone https://github.com/thebestwj/hugo-theme-wiki.git themes/hugo-primer

hugo server --theme=hugo-theme-wiki
```

### Customizing

#### config.toml

You can configure with these params in your blog's `config.toml`. Shown are defaults and most recommended configs.

```config.toml
# config.toml

hasCJKLanguage = true
# Code pen
pygmentsCodeFences = true
pygmentsUseClasses = true

# Enter a copyright notice to display in the site footer.
# To display a copyright symbol, type `&copy;`.
copyright = ""

[params]
# Chose Social Sharing Buttons you want to use.
shareTo = ["Twitter", "Hatena", "Facebook", "Pocket"]
# You may disable copyright sentence by setting this to false.
showFooterCredits = true
```

#### archetypes/default.md

It is also recommended to remove your site's `archetypes/default.md`, or copy Hugo-Primer's `archetypes/default.md` to your site.

```archetypes/default.md
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
categories:
tags:
keywords:
---
```

#### page-level params

- __showDate__ (default: __true__)  
shows the date on a post

- __comments__ (default: __true__)  
setting to false will hide disqus comments

- __toc__ (default: __true__)  
display the table of contents

- __categories__ (default: __an empty list__)  
a list of categories to display in the sidebar

- __tags__ (default: __an empty list__)  
a list of tags to display in the sidebar

- __math__ (default: __false__)  
If math.js is disabled for the site you can use this setting to enable it for a single page

- __keywords__ (default: __an empty list__)  
This adds a metatag to the page for listing keywords. This can be useful for SEO. 


Example usage where the defaults are overridden:

```md
---
showdate: false
comments: false
toc: false
categories:
- Diary
tags:
- Shopping
- Health
math: true
keywords:
- Cheese
- Milk
---
```

## Contributing

Issues and PRs are welcome. :)

## License

MIT (c) 2020 thebestwj

This Theme is modified from [Hugo-Primer](https://github.com/qqhann/hugo-primer) with original license: MIT (c) 2018 Qiushi Pan
