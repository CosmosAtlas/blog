---
title: "Creation Your Own Colorscheme"
date: 2020-09-10T20:21:29+08:00
author: "Wenhan Zhu (Cosmos)"
cover: "images/danqing-palette.png"
tags: 
- "colorscheme"
- "vim"
- "linux"
- "base16"
- "danqing"
keywords:
- "vim"
- "colorscheme"
description: "How to build your own colorscheme with base16"
showFullContent: false
draft: false
---

Modern text editors will highlight syntax when you are programming. As of
everything that is customization, many different colorschemes exists to
highlight syntax one way or another. The same idea can also apply to anything
with color. In my daily life, that translates to the color of by window manager,
and my terminal applications.

## Past favorite

Most people start by using the default colorscheme that came with your text
editor or the terminal. Then you discover the default options and changed to one
you like. For example, the [solarized
colorscheme](https://ethanschoonover.com/solarized/) is probably what everyone
have tried once. Personally I'm not a fan, but it is a thoughfully designed
colorscheme and understand why many people love it.

![Solarized Colorscheme](https://github.com/altercation/solarized/raw/master/img/solarized-dualmode.png)

[Gruvbox](https://github.com/morhetz/gruvbox) is a popular colorscheme that have
a yellowish tone to it. I've used this colorscheme for a long time and am really
satisfied with it.

![Gruvbox Dark](https://camo.githubusercontent.com/2fcf604967167347f15ca8be125d32b18db9bc28/687474703a2f2f692e696d6775722e636f6d2f476b496c38466e2e706e67)

[Nord](https://github.com/arcticicestudio/nord) is an arctic, north-bluish color
scheme that became really popular in the recent years. One advantage of nord is
it has been ported to many applications. So if you want to have your nord
colorscheme on some software, there's probably already someone that have done
that.

![Nord](https://raw.githubusercontent.com/arcticicestudio/nord-docs/develop/assets/images/ports/vim/overview-go.png)

## Why build your own

Although there already exists many beautiful colorschemes out there, sometimes
it just feels a bit off. Creating your own colorscheme solves this issue. But
creating a colorscheme you like takes some effort.

Due to the complexity of colors in terminal and how sometimes you wish the color
for a specific element is different, I started to add some tweaks to the
colorschemes. For example, I'll remove the background color in _vim_ so
transparency works as expected. When doing these edits, I started to wonder if I
can create a colorscheme that's really my own.

I started looking around on how to create a colorscheme. I've came across a
wonderful guide by _cocopon_: [_Creating Your Lovely Color
Scheme_](https://speakerdeck.com/cocopon/creating-your-lovely-color-scheme). I
would suggest you to give it a read, trust me, it's worth your time if you're
interested in colorschemes.

## Inspirations and color picks

Following _cocopon_'s slides, the first thing is to decide a theme. I've decided
to base on traditional chinese colors. These are colors used in China for
traditional chinese paintings. People back in the days rely on natural
ingredients to create paint, so the colors will have a unique taste to them.

### 丹青 (DanQing)

I decide to name my colorscheme danqing (丹青) which is a pronoun for Chinese
painting in Pinyin.

I used a website online to find traditional Chinese colors

- [_Chinese Traditional
  Colors_](http://ylbook.com/cms/web/chuantongsecai/chuantongsecai.htm)

The first thing is to decide on a shade of colors representing from the darkest
to lightest. I picked the chinese color 素 (which stands for raw color, e.g.,
the color of the [Xuan paper](https://en.wikipedia.org/wiki/Xuan_paper) used for
Chinese writing and paintings) and used the [tint and shade
generator](https://maketintsandshades.com/) to form the shade of colors from
dark to light.

Due to historical reasons, most colorschemes are based of 16 colors. This was a
limit for terminal color display limitations back in the days. Now 256 colors
and even 24bit full colors are supported by most terminals. However, the 16
colors is a good starting point to build the colors.

The first 8 colors will be the shade from dark to light. Which I already
generated previously.

Next, 8 more colors will have to be chosen. There are 6 conventional colors in
terminal besides white and black which are covered by our shade.

- Red
- Green
- Yellow
- Blue
- Magenta
- Cyan

And this gives us 2 more free colors.

I've used the colors website mentioned previously to find colors matching the 6
conventional colors that I like and tweaked them (a loooot of tweaking...) until
they look nature. For the additional 2 colors, I used a dark orange and dark
brown color.

## Building your own colorscheme --- the easy way

[Base16](https://github.com/chriskempson/base16) is an architecture for building
color themes based on 16 chosen colors. It is composed of 3 parts.

- Builder
- Template
- Scheme

Where the schemes are the actual colorschemes, the template stores the
information of how to convert a colorscheme into the format of a specfic
application. For example there is the _vim_ template for building _vim_
colorschemes. Builder is the tool to actually perform the action of building the
colorschme based on the scheme and template.

I stored the danqing colorscheme and build it for _vim_ and _Xresources_ using
the [base16-builder](https://github.com/base16-builder/base16-builder).

![danqing in action](/images/danqing-example.png)

I'm quite satisfied with the result and I have my own colorscheme!

Of course this colorscheme is not perfect. For example, the base16 _vim_
template is no where near as powerful as the full fledged Gruvbox _vim_
colorscheme. However, for me it's enough.

## Conclusion

If you're not satisfied with your existing colorscheme, or you want to scratch
your itch and create your own colorscheme, consider giving base16 a try. All you
need is a shade color to generate 8 colors from dark to light (or light to dark
if you want to have a light color scheme) and pick 8 other colors for
highlights. Combining that with experiments and tweakings until it fits your
likings.
