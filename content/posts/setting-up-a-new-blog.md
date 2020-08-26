---
title: "Setting Up a New Blog"
date: 2020-08-25T00:12:06+08:00
author: "Wenhan Zhu (Cosmos)"
cover: ""
tags:
  - "blog"
  - "life"
keywords:
  - "hugo"
description: "My approach to setting up a blog with Hugo"
showFullContent: false
draft: false
---

# Setting Up a New Blog

I have long since wanting to set up a personal blog. However, like many things
in life, it gets postponed forever. During this week long vocation, I decided
to finally set up my personal blog.

## Requirements

For my blog project, I've made the following requirements.

- Portable
- Posts in plain text
- Extensible

### Portable

I want to be able to blog on many devices, from _Windows_, _MacOS_ to _GNU/Linux_ based operating system. Or in other words, it should be manageable through a _git_ repository and easily deployable either with my own VPS or on platforms such as _GitHub Pages_ or _Heroku_.

### Posts in plain text

Being an open-source enthusiast and command-line lover, it is essential for me that the post files are in plain text. Locking behind a proprietary format or even software is unacceptable. There are many benefit of plain text files, but the biggest one for me is it'll still be the same 100 years from now and even if the software operating on them has been long gone in history, it is still easily to develop new software that works with it nicely.

### Extensible

It's hard to imagine something out there, be it the blogging infrastructure or available themes perfectly matches my taste and needs. So extensibility of the blogging setup is an important factor. It allows me to fix my itches when needed and always have the open ground for improvement.

## Choices and Decisions

### Choosing what to power the blog

The first is to decide on what to build the blog with. After some research online, it seems that there are 3 major options for blogging.

- Join a Blogging website (Medium, Blogger etc.)
- Cloud based blogging services (Word Express)
- Static website generators (Hexo, Hugo, Jykell etc.)

The first two options do not satisfy the portable requirements so it leaves me to static website generators. I've previously have experience with _Jykell_, in fact, _GitHub_ is build on _Jykell_ and it integrates nicely with _GitHub Pages_. 

So I've decided to try out the following static website generators.

- Hexo -- powered by _Nodejs_
- Pelican -- powered by _Python_
- Hugo -- powered by _Go_

I've decided to not to use _Jykell_ since it's based on _Ruby_. Unfortunately, although I had good experience with _Jykell_, _Ruby_ as a language have passed it glory days and it's popularity is declining year by year. To be more future proof, I've decide to look at other static website generators based on more vibrating communities.

#### Pelican

I had high hopes for Pelican since it's build on Python and came across some nicely looking blogs based on it. However, the project feels unpolished to the eye. I do believe the code quality and such have no problems, but I don't feel like jumping into the rabbit hole to fully customize my blog.

Maybe sometime I'll take another look at Pelican. But that'll be some other time... Maybe I should use Pelican for my knowledge base website, who knows, time will tell. : )

#### Hexo

Hexo at first glance looks really cool. The concept is cool, the themes library looks amazing. Upon trying to install locally, the problem arises. It took a very long time to install the required _node_ packages and the `node_modules` folder ends up around 90Mb. I tried some awesome themes like the _icarus_ theme and really liked it. However, every operation just feels slow. Website build time for a few test posts takes a few seconds while both Pelican and Hugo completes almost instantaneously.

#### Hugo

It leaves us to Hugo then. Hugo feels like a middle ground between Pelican and Hexo. It feels more polish and probably being less customization than Pelican. It's way faster according to some metrics on the web but it's themes and functionality aren't as cool as Hexo. It's expected to be less powerful than Hexo, since nothing is going to be better than something build on the same technology as the web itself...

I decided to go with Hugo in the end. It is a nice middle ground between Hexo and Pelican. On top of that, I really enjoy the speed _Go_ provides with Hugo.

### Where the blog runs

After decided on the tools, now it's time to pick a place to deploy the blog. With static website generators, there are also 3 options to deploy the blog.

- Self-hosting
- _GitHub/GitLab Pages_
- Netlify

Since I plan to run the blog behind _git_ on _GitHub_ anyway, I went with _GitHub Pages_. I'm not against _GitLab_ but just for now I use _GitHub_ more since it provides free pro version for me. If Microsoft ever did something, I'll probably jump ship to _GitLab_ or even on a self-hosted _Gitea_ instance.

## Themes

I've always like themes based on the terminal. Hugo have a few terminal based themes. After testing them out, I picked [_hugo-theme-terminal_](https://github.com/panr/hugo-theme-terminal) and powered the blog base on it.

## Customizing

### Setting up the comment section

I've always thought setting up a comment section is tough. It either requires using a complex infrastructure like Word Express, or have a complex server to support it. After looking up, it seems like I was over complicating the issue. All I need to do was register a service and paste a few lines of _html_ in the template.

I found a very interesting project called `utteranc.es` which is a hack that uses _GitHub_ issues to provide a lightweight comments widget. I followed the guide and quickly set up a fully featured comment section! A good start on customizing my blog.

### Copyright information

It turns out the theme I'm using already have this in mind. All I did was copy the CC by-SA 4.0 license info to the configuration file and it renders at the footer nicely.

### Dual language

I've seen this in many blogs where the author writes in two or three languages. Since I'm native in Chinese, I also want to write blogs in Chinese too. Hugo provides some infrastructure to manage multi language blogging, so that's a good start.

A simple way to do that is setting up the correct sections in the config file and suffix the posts in language codes. For example, both of the files below are the same post `my-first-post` but the suffix will tell which language it is written in. 

```text
my-first-post.en.md
my-first-post.zh.md
```

In the Hugo docs, they highlight the word "translation", I'm guess it assumes the user to write a same blog post in both languages so one acts as the translation as the other. There are also cool tips on how to automatically show a translated page exists on the blog post. Since I have no plans to write the same blog in multiple languages, I won't apply the tip. If in the future, I find myself with such need, I'll revisit this section.

The `hugo-theme-terminal` themes have a language selector built in. However, it seems to be broken. After some investigation, it turns out to be an easy fix. I've submitted a pull request to fix this issue. I'll update this post base on the result.

### Information pages

Alongside with the blog, most blogs have other sections that contain information about the blog owner.

- About page -- Information about the blog owner
- Tags page -- List of all tags

## Deploying 

Now the blog is set up and running. The only thing left is to deploy the blog. I won't list the details here since they vary a lot depend on your options. And there's already a ton of great material out there on the web. Additionally many of the information change from time to time, so it's best to refer to their official page.

Steps to deploy to _GitHub Pages_ with Hugo:

- [Create your _GitHub_ pages repo](https://pages.github.com/)
- (Optional) Get a domain
- (Optional) [Link the domain to your _GitHub pages_ repo.](https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site) -- Note DNS takes up to 24 hrs to propagate
- [Upload the built Hugo site to your _GitHub pages_ repo](https://gohugo.io/hosting-and-deployment/hosting-on-github/)

After these steps, the blog is up and running and accessible from the web!

## More to read

Hugo supports many content formats. Here's my other blog post on Hugo and asciidoc.

- [Hugo with asciidoc]({{< ref "posts/hugo-with-asciidoc" >}})
