---
title: "Picky Learnings"
date: 2021-02-15T14:04:36-05:00
Description: ""
Tags: ["jamstack", "web"]
Categories: ["jamstack"]
DisableComments: false
image: /images/online-test.svg
---

{{< episode-image "/online-test.svg" >}}

## :computer: dang, computers are picky

And, I knew this...but, nothing like an hour spent troubleshooting a needlessly simple oversight to drive home the point, right?

In trying to build this sample blog site on Netlify, I kept running into a build error having to do with a non-alphanumeric character in a shortcode.

I'd left a period inside of a sample shortcode I wrote to display an image. Hugo got mad. It far prefers for any non-alphanumeric characters to have quotes around them! :smile:

I followed that up with another quandry:

### baseURL Dilemma

I had not changed the baseURL in my config after pulling in and modifying the theme's config.toml.

By default, the baseURL is set to example.com which worked totally fine developing and previewing with hugo server locally.

When I built the site after resolving the shortcode error, though, all the styling was gone!

I swapped in the netlify address and, presto! :balloon: all is well once more.