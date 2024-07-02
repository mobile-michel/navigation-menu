---
title: README.md file
description: This README.md file list all the features and how it is constructed.
link-name: Readme
date: 2024-01-02
layout: layouts/default
tags: [primary, footer]
css2: /assets/css/menu.css
---
# Basic website built with Eleventy, LiquidJS & classless CSS

## Folder structure

- templates (content files) in ./
- includes in _includes/
- layouts in _includes/layouts/
- JSON files in _data/
- for a blog, create a folder blog/ with index.md + blog.json
- for CSS files, see stylesheet section below...

## Page layout

- _includes/layouts/base.liquid: head + body code
- _includes/layouts/default.liquid: HTML5 structure with ARIA landmarks and navigation includes
- _includes/navigation/primary.liquid with primary navigation links
- _includes/navigation/secondary.liquid for aside navigation links
- _includes/navigation/collection.liquid for previous & next links
- _includes/navigation/footer.liquid with footer navigation links
- _includes/copyright.liquid to include copyright information in footer

## Navigation links

- navigation links in the header: add the tag "primary"
- navigation links in the footer: add the tag "footer"
- for dropdowns in primary navigation, add the tag "dropdown" and create "navigation:" with the name of the tag
- for aside navigation, add the tag "secondary" and create "navigation:" with the name of the tag
- for previous & next links, create "navigation:" with the name of the tag

## Stylesheet

- the stylesheet works with tokens, many different files and is built any time there is a modification
- tokens is in _data/tokens.json
- the main file ./css.liquid built the stylesheet with a permalink to _site/assets/css/style.css and assemble this files:
  - _includes/css/reset.css
  - _includes/css/variables.css
  - _includes/css/base.css
  - _includes/css/flex.css
  - _includes/css/space.css
  - _includes/css/colors.css
  - _includes/css/navigation.css

## Package.json scripts
- "start": "npx @11ty/eleventy --serve",
- "build": "@11ty/eleventy",
- "build-gp": "eleventy --pathprefix '10b-basic'"

## Dependencies & misc
- "@11ty/eleventy": "^2.0.1"
- ready for GitHub Pages (.github/workflows/)

## eleventy.config.js
- there is no configuration file, so the default configuration is loaded