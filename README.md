
![markdown logo](assets/user/markdown.svg)

# ATL InfoSec 
## A mapping of Atlanta's Cyber, Information Security, and Privacy Community.

_`Last Updated: 7/7/2022`_ [`edit`](https://github.com/dandalpiaz/markdown-pages/edit/master/README.md)

Create a simple website that utilizes Markdown files for page content. No site generator necessary. Edit directly on GitHub! The pages and files in the [GitHub ![GitHub Logo](assets/user/github.png) repository](https://github.com/dandalpiaz/markdown-pages) are rendered on [this website](https://dandalpiaz.github.io/markdown-pages) via GitHub Pages. 

## Table of Contents


- [Getting Started](#getting-started)
- [File Structure](#file-structure)
- [Styles](#styles)
- [Limitations](#limitations)
- [About](#about)


## Getting Started 

To set up a site, simply fork or copy the files from the [markdown-pages repository](https://github.com/dandalpiaz/markdown-pages) into your own repo, and then enable GitHub pages for your repository. Steps 2 and 3 in this [Quickstart for GitHub Pages](https://docs.github.com/en/pages/quickstart) show how this is done in the interface. Other steps can be ignored.

## File Structure

```
markdown-pages/
|---assets/
|------user/
|	   |---favicon.png
|	   |---example.png
|---pages/
|	|---sample-page.md
|	|---sample-page-2.md
|---index.html
|---README.md
```

### README.md

The `README.md` file will provide the content for the homepage of your site. Simply author the file using [Markdown syntax](https://www.markdownguide.org/basic-syntax/).

### index.html

The `index.html` file does the magic of converting Markdown to HTML. It will also look for a heading level 1 (h1) on the current page and prepend it to the site title. You can add your site title by modifying this line in the header:

```
&lt;title&gt;Markdown Pages&lt;/title&gt;
```

There are other lines in the header that you may want to edit as well, such as the meta description and the favicon image name/location.


### Pages

Additional pages can be added to the `pages` directory, using Markdown files. To add a link to an additional page, for example, `sample-page.md`, the following link structure can be used: 

```
Check out the [sample page](?page=sample-page)
```

Check out the [sample page](?page=sample-page).

### Assets

Images and other files can be added to the `assets/user` directory and linked as needed. 

## Styles

### Dark/Light Mode

The site will include a dark/light mode toggle button by default. When adding images to a page, consider adding images that will contrast well against both a light and dark background.

### Syntax Highlighting

Syntax highlighting will automatically be applied to code blocks, for example:

```
def my_function():
  fruits = ['orange', 'apple', 'pear', 'kiwi', 'banana']
  for fruit in fruits:
    if fruit == 'banana':
        print(fruit)

my_function()
```

## Limitations

With no templating engine in use, and a reliance on Markdown for content creation, this project does have a number of limitations:

- **Local Development** - since the site uses XMLHttpRequest to grab content, a local web server will be needed if you want to see things locally, e.g. `python -m http.server`. However, editing directly in GitHub is part of what is convenient about the project.
- **Limited element options** - if the element you're trying to use exists in Markdown, the converter should be able to render it as HTML, but this will exclude a lot of more advanced HTML elements.  
- **No custom layouts** - Markdown used in this way is fairly linear, so you won't be able to do a columns and fancy layouts without a lot of extra work.
- **No semantic menus/landmarks** - the converter is set to take the Markdown content and place it inside the `<main>` landmark. Other landmarks aren't currently represented. 
- **No dynamic/reusable content** - currently no mechanism to reuse content across mulitple pages.

## TODO

- Eliminate 'pages' directory so that GitHub and hosted site can find assets using the same relative paths?
- Google Translate popping up?

## About
This site was created to summarize the Cyber Security, Information Security, and Privacy community in Atlanta, Georgia, USA.  This is a non-commercial project.


### Want to make a contribution?
You have a few options.  

* Create an [issue](https://github.com/bricedobson/atl-cyber-infosec-privacy/issues).
OR
* Clone the repo, Make the edit yourself, and submit a PR in our [repository](https://github.com/bricedobson/atl-cyber-infosec-privacy).
OR
* Email us at <insert>

### Credits
This project was inspired by [TrailOfBits NYC Infosec](https://www.nyc-infosec.com/https://github.com/trailofbits/nyc-infosec)
Powered by [GitHub Pages](https://pages.github.com), [Jekyll](https://github.com/jekyll/jekyll), and [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes).
This site is maintained by [Brice Dobson](https://github.com/bricedobson)
