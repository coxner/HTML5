# HTML5

This repository is made to represent what I have learn while reading through [HTML5 The missing Manual](http://shop.oreilly.com/product/0636920029243.do) The code examples are there's I have manipulated them and explained what the code itself is doing. I have done this to help me retain information and have a guide to look back on but also display that I have a solid understanding of HTML5 markup.

## Resources

Browser Support: [Here](https://caniuse.com/)
Browser Statistics: [Here](http://gs.statcounter.com/)
Feature Support: [Here](https://modernizr.com/)
Web Accessibility Initiative: [Here](https://www.w3.org/WAI/)
HTML5 Outliner: [Here](https://gsnedders.html5.org/outliner/)

The `<big>` element has been discarded in HTML5 however the `<small>` tag is still used and has been adapted to represent small print. Example: small writing on the bottom of a contract.

In HTML5 the meaning of the `<hr>` tag has changed. It now represents a break in subjects and is used when transitioning from one subject to another.

The `<s>` tag is no longer supposed to be used for crossing out text. It not represents text that is not longer accurate or relevant. It still crosses out text the same way it did before only the meaning of it has just changed.

The `<strong>` tag is for text of _strong importance_. It has to stand out from its surroundings.

The `<b>` tag is for bolded text. But it does not have more importance then the rest of its text.

The `<em>` tag is used to emphasis words.

The `<i>` tag is used to italicize words. But the word itself has no extra emphasis.

The `<address>` tag has shifted its meaning as well. It is not appropriate to use a postal code within it any more. It is, meant to provide contact information for the developer of a HTML document. It commonly stores an email or website link.

To other interesting tags are the `<wbr>` tag that causes a word break only if it doesn’t fit in the space it is provided. The `<nobr>` which can be used to prevent a word from breaking if there is a space between it.

Check out the use of the `<detail>` and `<summary>` tag. When the heading is code written within the summary tag is displayed.

## A new page layout

In the _improvedLayout.html_ file you will see the new way pages are marked up using HTML5. The `<article>` tag is used to wrap around a whole piece of content. This content can be something like a news story or a blog post. If one of your post contains a header and a sub header you can wrap the both of them within a `<hgroup>`. A `<figure>` element refers to a image that is **separate** from the text but referred to within the text. The `<aside>` tag is a great way to create sidebars as you can see in the coding example. The `<header>` tag has **two** uses you can use it to title your webpage or you can use it to title some content.

###Useful tips
Adding `<header>` tags as titles to content helps people navigate your site who are using screen readers.
Your website should only contain **1 `<h1>` tag**. It makes your site more accessible to screen readers. The level 1 heading is made to be unique and should clearly tell the search engine what the content of your site holds. The popularity of using more then one h1 tag to mark different sections of a site is growing. A `<section>` tag is more specific then a `<div>` tag and is intended to be used with any block of content that starts with a heading.

#### Useful CSS

`article, aside, figure, figcaption, footer, header, hgroup, nav, section, summary { display: block; }` Web browsers that don't support HTML5 elements won't know how to display them. This line of CSS will provide a fall back if your user is using an unsupported browser.
