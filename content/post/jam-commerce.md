---
title: "Jam Commerce"
date: 2021-02-12T11:08:52-05:00
draft: false
---

# E-Commerce with the Jamstack

## Meetup Summary

I attended a [virtual Meetup yesterday](https://www.meetup.com/JAMstack-Toronto/events/275874245/) :video_camera: that was put on by [Jamstack Toronto](https://www.meetup.com/JAMstack-Toronto/) discussing the various ways in which we have made e-commerce sites, and the many opportunities now available to expand past the typical, all-in-one approaches (Wordpress etc).

I've been excited about this for a while, so it was less revolutionary an idea for me and more of a continued examination of the options availalbe.

## Our current issue

At Cups, we have a pretty nice site built on Wordpress. We re-did this about two years ago, and it's waaaay better than what we had previously.

However, **it's slow:** :snail:

![lighthouse score](/images/lighthouse-2.12.21.jpg)

We've tried speeding it up with some caching plugins, but it has reached a point where it really feels like we're having to do way more work than we should to just get a snappy website.

And the dashboard runs slow too. It takes seconds to go through menus, create new products and save each and every modified property of the items....

And, for Pete's sake, we're a coffee shop. It's not super complicated. :frowning:

We have a pretty simple online store of coffee, some retail items, and that's really it. We don't even need it to do any inventory tracking for us. When we run out of a coffee to roast, we simply turn the item off.

We've got under 100 items on the store, and yes, all the coffees have modifier selections for different grind types. But, we're not talking thousands of items in a store.

It should not have to be slow.

## Enter my new infatuation with the Jamstack.

For whatever reason, I've taken a liking to Hugo over the other big static site generators as my first to learn, and I'm following along with this [blog post](https://snipcart.com/blog/hugo-tutorial-static-site-ecommerce) by Snipcart to get a pretty darn nice little one page site up and running.

I'm still navigating my way around the Go templating in Hugo, but that's really my biggest hurdle as I hook up [Hugo](https://gohugo.io/), [Snipcart](https://snipcart.com/) and [Forestry](https://forestry.io/).

Getting the sample site up and running with their given code has made me realize there's so much to be gained by shaving off those annoying seconds of page loading both as a user and as a maintainer.

Look forward to showing you updates as I go along! :smile: