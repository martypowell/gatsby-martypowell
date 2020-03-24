---
title: Hello World
date: "2020-03-18T23:46:37.121Z"
template: "post"
draft: false
slug: "hello-world"
category: "Gatsby"
tags:
  - "Hello World"

description: "This is my first Gatsby blog entry. Let's see how this goes."
socialImage: ""
---

I have decided to start updating my portfolio and wanted the ability to have a blog. I am not sure why, but I have always heard it is good to write.

I will attempt to document my success and failures in this entry, in setting up [gatsby](https://www.gatsbyjs.org/) to create a blog.

## Starter Template

After quickly going through the [quick started guide](https://www.gatsbyjs.org/docs/quick-start/), I decided to go with the [gatsby-starter-lumen starter template](https://github.com/alxshelepenok/gatsby-starter-lumen.git) based on the [Working with Starters Recipe](https://www.gatsbyjs.org/docs/recipes/working-with-starters/).

The reason I chose this template was because it had a blog, which I was looking for, and supported markdown which was another big thing for me. The template and list of blog items, seemed like something I could easily modify if I wanted to.

So far the docs are very good, but it was hard to find this starter template after going back to the [starters library](https://www.gatsbyjs.org/starters) after I had already installed it and forgot the name.

## Running For the First Time

I added a `start` script to the `package.json` to alias the `develop` script that already existed. I did this mainly out of habit from doing a lot of create-react-app development. Everything ran as expected.

Viewing the terminal, I noticed that there was a link to `http://localhost:8000/admin`. So I navigated to that Url. It took me to a Netlify prompt. Without getting too deep into it, after some research I decided to skip past the admin section for now and to try and see if I could manually add a post to the blog.

**Note**: I will come back to this later.

## Adding My First Blog Post

I scanned the project structured and got lucky guessing that blog entires might live in the `content` folder. I opened it up and sure enough there was a folder named `posts`.

I copied one of the existing pages and modified it for my needs. If you couldn't figure out by now, this is the blog post I am writing now. After hopping back over to my localhost, my post was visible and I was able to see what content I had added so far #:raised_hands:. (I may have also installed emoji support at this point.)

This was also a good point at which I did a famous `initial revision` commit and pushed up whatever changes I had made to [github](https://github.com/martypowell/gatsby-martypowell).

## Modifying Some Styles

Next step was to change some of the styles. I figured I would try the following minor changes.

- Change font families for headings and body text
- Change link colors

### Changing the Font Family

After some search around, I found that `src\components\Layout` contained the head for the site. I added the google fonts link that I had hoped to use to that component and committed that change.

Much to my liking there is was a variables file located at `src\assets\scss` which contained a variable called `$typographic-font-family`. I was able to add the font I wanted to be the default as the value for this variable. I noticed that there was not heading variable available, so I created on based on my heading font, and adjusted the `src\assets\scss\base\_generic.scss` to use that variable for headings instead of the default.

That was it, fonts updated.
