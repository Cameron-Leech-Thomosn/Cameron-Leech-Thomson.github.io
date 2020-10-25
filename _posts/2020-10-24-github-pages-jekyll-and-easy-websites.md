---
layout: post
title: "GitHub Pages, Jekyll, and Easy Websites"
date: 2020-10-24
excerpt: "A brief summary on the way this site was made."
image: "/images/GitHubPages.jpg"
caption: "GitHub Pages"
credit: "https://pages.github.com/"
---

## This Site
This site was created for free by me, with the use of [GitHub Pages](https://pages.github.com/). GitHub Pages is GitHub's hosting platform, allowing you to create sites for yourself of for an individual repository. It's really easy to set up, and you can find out how [here](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages). Pages allows you to choose from a few pre-set themes that give your site a little more flair, or you could go and find a custom one that suits you, or go ahead and make one yourself! The custom theme that I'm using is called Massively, and you can find out more about it [here](https://github.com/jekyllup/jekyll-theme-massively). All of the themes use [Jekyll - a static site generator](https://jekyllrb.com/). You can use it to style your site using different layouts and pages based in what you'd expect (HTML, CSS, JavaScript), and add content by using different mark-up files. 

### Content
Content for each page is inside of a file containing a mark-up language. For example, I'm using markdown (.md) files. In each file, you must specify the attributes that will be used in the layout file. For example, in the [previous post](https://cameron-leech-thomson.github.io/blog/welcome-to-my-site/) I put up, the attributes look like this:
```markdown
    ---
    layout: post
    title: "Welcome to My Site!"
    date:   2020-10-21
    excerpt: "This is the first post on my shiny new portfolio site!"
    image: "/images/post1.jpg"
    caption: "Photo by Ilya Pavlov on Unsplash"
    credit: "https://unsplash.com/photos/OqtafYT5kTw?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink"
    ---
```
The attributes here are accessed in a HTML file, and then used to fill the slots for various pieces of content. The main bulk of writing done in a post is done after the "---".

### Layouts
Each layout is just a HTML file, that creates the setting for the content. However the actual content is not in the HTML, but is in a mark-up file. To pull the information from the mark-up files, you'd access it like this:
Say you're after the markdown attribute 'title' in:
```markdown
    title: "Post Title"
```
Which you're trying to put in the main header for your page. You'd set the HTML up like this:
```html
    <header>
    <!-- {% raw %} -->
        <h1 class = "title">{{page.title}}</h1>
    <!-- {% endraw %} -->
    </header>
```
In this instance, the call "{{page.title}}" is where you retrieve the title of the page itself. You'd also preface any attribute you're after with "page." then the name of the attribute. HTML takes in the string and runs it essentially like it would if you were to write it there normally. For example, if you wanted to embed a URL, you'd do it like this:
```html
<!-- {% raw %} -->
    <a href = "{{page.url}}">Click Here!</a>
<!-- {% endraw %} -->
```
Images would work in exactly the same way too.

## Learn More
If you'd like to learn more about Jekyll, you can [click here](https://jekyllrb.com/) to be taken to the Jekyll website. If you'd like to learn more about GitHub pages, you can [click here](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages) to be taken to the Pages documentation. If you'd like to find out more about markdown - the language I use for the site's content, you can find out [here](https://www.markdownguide.org/). I'd recommend having a play with it, even if you don't have a reason for a website. It's just good fun, and it's free!

Have a nice day!