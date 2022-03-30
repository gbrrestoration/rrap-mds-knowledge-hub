---
layout: default
title: Development Documentation for generating RRAP-IS M&DS documentation  
nav_order: 4
has_children: true
---

# [Local](https://just-the-docs.github.io/just-the-docs/#local-installation-use-the-gem-based-theme) Development 
See https://just-the-docs.github.io/just-the-docs/#local-installation-use-the-gem-based-theme for setting up for local development.
___
## Linux development
Follow the guide in the link above
___
## Windows development
Use the Jekyll Windows installer --> https://jekyllrb.com/docs/installation/windows/
There are a number of packages that are not included which you will need to add separately;

1. ```gem install wdm```
1. ```gem install webrick```
___
## During documentation 
To see your local changes run  ```jekyll server --config _config_development.yml``` 
see https://jekyllrb.com/docs/usage/
___
## Further documentation on Just-The-Docs
https://just-the-docs.github.io/just-the-docs/

___
## Markdown
Cheat sheet --> https://www.markdownguide.org/cheat-sheet/

Markdown tables can become a little difficult to build, so here is a link to a online tool to make the process a little easier, MD Table builder --> https://www.tablesgenerator.com/markdown_tables

Here is examples of our callouts

{% include warning.html content="Warning example text." %}

{% include danger.html content="Danger example text." %}

{% include success.html content="Success example text." %}

{% include notes.html content="Note example text." %}