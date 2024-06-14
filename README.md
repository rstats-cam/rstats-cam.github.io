# CambRidge Website
This is a repo for the Quarto website for the CamBridge User Group

It contains a home page, events, page and blog posts.

## Contributing
### Without write access
Corrections, suggestions and general improvements are welcome as [issues](https://github.com/thomaszwagerman/cambRidge-site/issues).

You can also suggest changes by forking this repository, and opening a pull request. Please target your pull requests to the `main` branch.

### With write access
You can push directly to main for small fixes. Please use PRs to main for discussing larger updates.

## Directory Structure
This a "classic" Quarto website, but also contains blog posts.

This means there is a slightly different directory structure than what you might be used to.

```
project
│   _quarto.yml
|   index.qmd
│   events.qmd
│   blogs.qmd # This is a listing file for a blogs in /posts
|   styles.css
|   ...
│
└───posts/
│   │   _metadata.yml
│   │
│   └───YYYY-MM-DD-post-description
│       │   index.qmd
│   
└───docs/ # Contains all html files rendered on Github Pages
    │   index.html
    │   events.html
    |   ...
```

## Adding a blog post
New blog posts should be created in the `posts/` directory.

You can copy the `YYYY-MM-DD-post-description` folder, this is a template folder.

Please use the same naming format to keep the ordering of posts consistent.

This folder contains an `index.qmd` file - do not rename this file. It has the following yaml header:

```yaml
---
title: "blog post title"
description: "blog post description (appears underneath the title in smaller text) which is included on the listing page"
author:
  - name: Thomas Zwagerman
    affiliation: British Antarctic Survey
date: 06-14-2024
categories: [Quarto, R, Cambridge] # self-defined categories
draft: true 
---
```
Update these details for you blog post. The `draft: true` header prevents publication. When you have finished your blost post, change it to `draft: false`, re-render and push your change (or open a Pull Request, without edit permissions), to publish the post. 

For a detailed breakdown refer to [Quarto's Creating a Blog documentation](https://quarto.org/docs/websites/website-blog.html).

## Adding an event



