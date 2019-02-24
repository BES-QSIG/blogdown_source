BES QESIG Website
===

## Overview

This repository contains the source materials for the [BES QESIG Website](https://bes-qsig.github.io/). In order to make updates to the website, you will need to clone both this repository and the [bes-qsig.github.io](https://github.com/bes-qsig/bes-qsig.github.io) repository to your local computer. 

Any changes to be made, should be made in the `blogdown_source` repository (this one), then to push them to the website, run the command `blogdown::build_site()` in R. 

Finally, ensure that changes to **both** repositories are committed and pushed to Github. Your changes will then be visible on [BES QESIG Website](https://bes-qsig.github.io/). 

## Making changes

The site has been built using blogdown. See [blogdown: Creating Websites with R Markdown](https://bookdown.org/yihui/blogdown/) for documentation. 

In summary, any content is stored in the `content/` directory in a folder with the same name as the page. For example, blog posts are stored in the `post/` folder. Changes to any of the items on the home page (e.g. about, contact etc.) can be made from the `home/` folder. 

To create new blog posts and events, a new folder should be created in the relevant folder. The name of this folder will be the URL link. Within this folder, create a .md file containing the content (see `themes/hugo-academic/archetypes/` for template .md files to use). 

To create new course documentation, the .md file will go directly in the `courses/` folder. See the Advancing your R course for an example of how to set this up. It's important to update the `[menu.courses]` section to ensure that the sidebar menu is correct. 

## Adding a section

Create a new folder in the `content/` directory with the same name as the new section. 

Into `config.toml` add a new navigation link. These are towards the bottom of the file and take the structure
```
[[menu.main]]
  name = "Home"
  url = "#about"
  weight = 1
```
`weight` controls the order of the section on the menu bar. 

## Questions

If you get stuck making updates, please contact the [quantitative](mailto:quantitative@britishecologicalsociety.org) email address, or raise an issue on this GitHub repository. 


