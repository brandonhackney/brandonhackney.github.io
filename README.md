# Site Maintenance Guide

The main page displayed is `index.md`. 
It gets converted to HTML by and uses CSS from GitHub's [Minimal theme](https://github.com/pages-themes/minimal).
Any time you make a change to this site, 
whether that be one of the documents or any of the content they reference,
the HTML has to be regenerated, and the code that does it takes a few minutes to run.
So be patient when testing updates.

The sidebar content with my picture and links is actually governed by two separate documents:

- Portrait and title are dictated by `_config.yml`
- Links are defined in `_layouts/default.html`, under "CUSTOM SECTION"

The page header with site navigation links is defined by a third document, under `_includes/head-custom.html`.

You can build more pages as markdown documents, but when linking from an existing page 
(or the header document), you need to reference an **HTML** version that may not exist yet 
(i.e. NOT the source markdown document). 
That's fine—see the first paragraph.

## Local testing

As stated before, this website uses an external themeing engine. 
It requires Ruby to build the HTML pages. This happens on-the-fly on the web, but to do it locally:

1. Open a terminal and run `chruby 3.3.6`.
2. `cd` into a clone of the [Minimal](https://github.com/pages-themes/minimal) repo
3. Once properly set up, run `bundle exec jekyll serve`
4. Open a web browser and visit [localhost:4000](localhost:4000)

### Explanation

I had to install an *alternate* version of Ruby (similar to what you do with Python), 
but started running into permission issues. 
I followed [this guide](https://stackoverflow.com/questions/51126403/you-dont-have-write-permissions-for-the-library-ruby-gems-2-3-0-directory-ma) to get around it.



