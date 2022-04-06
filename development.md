---
layout: default
title: Development Documentation for generating RRAP-IS M&DS documentation  
nav_order: 4
has_children: true
---
{: .no_toc }
# User Documentation (RRAP M&DS Knowledge Hub)
<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

We are using a Jekyll Site to host documentation, and the 'Just-The-Docs' for theming. 

Documentation repository is hosted on Github [here](https://github.com/gbrrestoration/rrap-mds-knowledge-hub)

There are a number of ways to edit/develop the documentation:

* If making small changes (fixing a spelling error) this can be done within GitHub itself using the local editor
* If making large/many changes you should clone the repository and make the changes and validate on your local machine prior to pushing back to the repository.  After pushing back to the repository the changes will be built and deployed on GitHub → https://gbrrestoration.github.io/rrap-mds-knowledge-hub/
* If making structure changes or adding complex html elements to be included with the markdown it would be best to have a local environment to build the site. See the repository development.md for steps in setting up your local environment  

___
## Local Development Environment setup
### Linux development
Follow the guide [local installation using the gem based theme](https://just-the-docs.github.io/just-the-docs/#local-installation-use-the-gem-based-theme)
### Windows development
Use the [Jekyll Windows installer](https://jekyllrb.com/docs/installation/windows/) 
There are a number of packages that are not included which you will need to add separately
1. ```gem install wdm```
1. ```gem install webrick```

___
## Documentation writing/development 
Documents are written using [Markdown](https://www.markdownguide.org/cheat-sheet/) syntax

The Jekyll site is built with ```jekyll b``` and the servered with ```jekyll server --config _config_development.yml```, note that we use a specific ```config.yml``` for development as the theme is local and we include this file in the site. 

After pushing code back to the repository GitHub actions will build and deploy the site using ```config.yml```

See Jekyll [notes](https://jekyllrb.com/docs/usage/) for further documentation on Jekyll usages 

___
### Further documentation on Just-The-Docs
[Just the Docs](https://just-the-docs.github.io/just-the-docs/)

___
## Markdown
[Cheat sheet](https://www.markdownguide.org/cheat-sheet/)

Markdown tables can become a little difficult to build, so here is a link to a online tool to make the process a little easier, [MD Table builder](https://www.tablesgenerator.com/markdown_tables)

Here is examples of our callouts
<table>
  <tr align=center>
    <th>Raw</th>
    <th>Result</th>
  </tr>
  <tr align=center>
    <td text-align=center>{%raw%}{% include warning.html content="Watch out" %}{%endraw%}</td>
    <td text-align=center>{% include warning.html content="Watch out." %}</td>
  </tr>
  <tr align=center>
    <td>{%raw%}{% include danger.html content="DO NOT ENTER." %}{%endraw%}</td>
    <td>{% include danger.html content="DO NOT ENTER" %}</td>
  </tr>
  <tr align=center>
    <td>{%raw%}{% include success.html content="Well done!" %}{%endraw%}</td>
    <td>{% include success.html content="Well done!" %}</td>
  </tr>
  <tr align=center>
    <td>{%raw%}{% include notes.html content="You can do it" %}{%endraw%}</td>
    <td>{% include notes.html content="You can do it" %}</td>
  </tr>    
</table>