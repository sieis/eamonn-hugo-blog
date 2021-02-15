---
title: "Hugo Podcast Shortcode"
date: 2021-01-06T15:43:07-05:00
draft: false
---
I have been struggling to get a codeblock to display a shortcode for illustration without Hugo actually executing the block. Since it's simply trying to do what it's supposed to, I'm not too angry with the code. :smile:

Custom shortcodes are how you can introduce particular behaviors into your Hugo project, and in my case, how I am embedding podcast players into blog posts.

The shortcode is the simple one I created for the Transistor podcast player to be displayed like this:

{{< transistor 70ef5a7e >}}


    {{ < transistor 70ef5a7e >}}
    code line

And here's what's happening in the shortcode html itself. Nothing fancy, but it works fine, and is a good introduction into creating a simple, custom shortcode.

    <div class="pod-player">
      <iframe width="100%" height="180" frameborder="no" scrolling="no" seamless
        src="https://share.transistor.fm/e/{{ .Get 0 }}"></iframe>
    </div>

The only necessary piece you'll need to input is the episode id from Transistor. I got this by going to the [shareable social media landing page](https://share.transistor.fm/s/70ef5a7e) available for every Transistor podcast that is published. It's also viewable within the embeddable player HTML generated.

Speaking of that embeddable player from Transistor, couldn't we just throw that iframe into our markdown file, you ask:question:

Well, no. At least not after [Hugo 0.60.0](https://discourse.gohugo.io/t/ raw-html-getting-omitted-in-0-60-0/22032) disallowed it. Normally, inline html is fine in markdown files. Though if you check out that article, there's still a way to allow it in Hugo:

>In your config enter:
>
>     [markup.goldmark.renderer]
>     unsafe= true

    <iframe width="100%" height="180" frameborder="no" scrolling="no" seamless src="https://share.transistor.fm/e/70ef5a7e"></iframe>

<iframe width="100%" height="180" frameborder="no" scrolling="no" seamless src="https://share.transistor.fm/e/70ef5a7e"></iframe>