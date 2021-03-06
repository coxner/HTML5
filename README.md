# HTML5

This repository is made to represent what I have learn while reading through [HTML5 The missing Manual](http://shop.oreilly.com/product/0636920029243.do) The code examples are there's I have manipulated them and explained what the code itself is doing. I have done this to help me retain information and have a guide to look back on but also display that I have a solid understanding of HTML5 markup.

## Resources

Browser Support: [Here](https://caniuse.com/)  
Browser Statistics: [Here](http://gs.statcounter.com/)  
Feature Support: [Here](https://modernizr.com/)  
Web Accessibility Initiative: [Here](https://www.w3.org/WAI/)  
HTML5 Outliner: [Here](https://gsnedders.html5.org/outliner/)  
Landmark Roles: [Here](https://www.w3.org/TR/2017/NOTE-wai-aria-practices-1.1-20171214/examples/landmarks/index.html)  
Microformatting: [Here](http://microformats.org/wiki/what-are-microformats)  
hCard Microformatting: [Here](http://microformats.org/wiki/hcard)  
hCalendar Formatting: [Here](http://microformats.org/wiki/hcalendar)  
Microdata: [Here](https://www.w3.org/TR/microdata/)  
Microdata itemtype: [Here](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemtype)  
Microdata itemprop: [Here](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemprop)  
Microdata from Schema: [Here](http://schema.org/docs/gs.html)  
Google Rich Snippets: [Here](https://developers.google.com/search/docs/guides/mark-up-content)  
Rich Snippets tester: [Here](https://search.google.com/test/rich-results)  
Regular Expression: [Here](https://www.w3schools.com/jsref/jsref_obj_regexp.asp)  
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

### Useful tips

Adding `<header>` tags as titles to content helps people navigate your site who are using screen readers.
Your website should only contain **1 `<h1>` tag**. It makes your site more accessible to screen readers. The level 1 heading is made to be unique and should clearly tell the search engine what the content of your site holds. The popularity of using more then one h1 tag to mark different sections of a site is growing. A `<section>` tag is more specific then a `<div>` tag and is intended to be used with any block of content that starts with a heading.

#### Useful CSS

`article, aside, figure, figcaption, footer, header, hgroup, nav, section, summary { display: block; }` Web browsers that don't support HTML5 elements won't know how to display them. This line of CSS will provide a fall back if your user is using an unsupported browser.

## Meaningful Sematic Tags

#### The &lt;time&gt; tag

The `<time>` tag is extremely useful because it allows programs like search engines to extract data from your website. It has two uses to provide you where a date/time is being used in your markup and provides a easy way for programs to extract date/time values from your markup.

An example of time is use is `<time>2018-06-25</time>`. However say we want to display a date to our user in a different format but keep our site compaitable with search engines. That is where the datetime attribute comes into play. Now we can present a date to our user like `<time datetime="2018-06-25">June 25 <sup>th</sup></time>`. Lastly you can specify a time with a date by following this markup `<time datetime="2018-06-25T12:30">June 25<sup>th</sup> at 12:30</time>` by putting a T at the end of our date followed by the time of the event you can see it is fairly simple to specify a time with a date. There is another attribute that is useable with time and that is the pubdate attribute.

#### The &lt;output&gt; tag

Another sematic tag that has been added is the `<output>` tag. It primarily a placeholder that your markup can use to hold a piece of caculated information. This can be seen in _BmiCalculator.html_ where the output tag is wrapped around the result returned to the user. There are two other attributes you can provide the output tag that have no effect on the results but just provide additional information on where the output tag is getting its information from. The form attribute indicates the form that controls the output tag and the for attribute list the ids used to perform the calcualtions.

#### The &lt;mark&gt; tag

The final tag will be looking at is the `<mark>` tag. The mark tag is used to highlight a section of text and is primarily used when quoting someone else or you want to bring attention to a section of text. By default the background color of the mark tag is a highlighter yellow. You can see in the code example _Mark.html_ how we could change the highlight color if we wanted to.

If you use the `<mark>` tag in your markup you should provide this simple fallback for browsers that don't support HTML5 elements.

`mark {`  
 `background-color: yellow;`  
 `color:black;`  
`}`

## ARIA (Accessible Rich Internet Applications)

Aria is known as a dev standard that allows devlopers to provide information in their markup for screen readers. It is most commonly done through the role attribute which defines what a elements purpose is. For more information on how to assign roles within your webpage [click here](https://www.w3.org/TR/2017/NOTE-wai-aria-practices-1.1-20171214/examples/landmarks/index.html)

## Annotating HTML5 Sematic Elements

What is sematic content?

### Microformatting

Microformatting is a simple way that you include meta data within your webpage. It is commonly used to HTML patterns for things like people, blog post and events. They are a way you can provide. It allows programs to extract information from your webpage that is marked up with microformats. You can read more [here](http://microformats.org/wiki/what-are-microformats)

Contact details are represented on a website with hCard. Microformats work off of the class attribute which is commonly used for styling. Depending on the data your are marking up their is a set standard on how you should name classes so data can be extracted. **To create a hcard you need a base element thats class attribute is vCard. Within the hcard you need a formatted name, the name must have the class of fn**. These are the two main attributes needed for a hCard however you can add more. Check out _hcard.html_ to checkout how to style contact details. Check out this [link](http://microformats.org/wiki/hcard) on hCard formatting.

_Useful tip:_ When writing hcard markup wrap block level elements in `<div>` tags and inline elements in `<span>` tags. Use `<br>` to shift from one `<span>` line to another. This is also represented in the _hcard.html_ file.

_Useful tip:_ You can add the CSS style `display:none` to any element of the markup if you want it to be represented in the microformatting but not displayed on the site.

Another microformat is hCalendar which is used for providing metadata to events. Similar to the hCard element we start with assigning the class name vevent to our base element. Inside you vevent element two classes must be present dstart to represent the start date and summary to represent the description. More information on hCalendar can be found [here](http://microformats.org/wiki/hcalendar).

### Microdata

Another common method used to annotate sematic tags is microdata. The major difference between the two is microdata introduces new attributes into markup and does not use class attributes like microformatiing does. More information [here](https://www.w3.org/TR/microdata/)

When starting a new sematic area on content with microdata the first attribute that must be used is `itemscope` which declares that you are creating a sematic section of code. The second attribute that must be used is `itemtype` which specifys the type of data being encoded. It is a unique attribute that must contain the url of the vocabulary that is being used to define the `itemprop`. More can be read [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemtype).The final attribute needed is known as `itemprop`. This is where the important information of your sematic code is stored. I would write my own markup to represent the structure of microdata but feel as if a better example can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemprop).

### RDFA

### JSON-Ld

## Forms

### Basics

The first step to creating a form is start with the opening `<form>` tag. In between the opening and closing form tag is where all the form controls and fields are stored. We can also tell the form where to send data when it is submitted through the action attribute.

### Dividing our form

We can divide our forms into logical sections that make sense. When indicating the start of a new section we use the `<fieldset>` tag. When providing this new section of code with a title we use the `<legend>` tag. As you can see each piece of information you want the user to submit in done with a `<label>` tag and a `<input>` tag.

### The type attribute

Check out how the type attribute affects the appearence of the input box. Try typing in the box with `type="password"` notice how the output is affected. By setting `type="checkbox"` we can give the user a checkbox they can check and uncheck. Another thing we can do with the type attributes is provide them values that make them buttons. The two most popular ones are `type="submit"` and `type="reset"` the submit buttons sends form data to its destinantion and reset clears all the information the user has in input boxes. **Buttons need javascript code with them to function**.

### Using placeholders

Using placeholders in forms is essetntial in providing infomation to users on what should be entered in each input. Everyone of us has seen placeholders in forms before. They are done with the attribute `placeholder="placeholder_value"` you can observe them in use in _forms.html_.

### Autofocus

When a user visits the page with your form on it you may want to place the cursor in a input box by default. This is done with `autofocus` as you can see in _forms.html_ `autofocus` is placed in the name input box so by default when the page loads the cursor is placed there.

### HTML5 Validation

If we have a input box that the user **must** provide info for we provide it with the attribute `required`. The problem with the required attribute is that there is no visual que that tells a user that this input is required. Thats why in _forms.html_ we provide a \* beside the label that is required. Validation only occurs when the user clicks the submit button. The browser checks the fields from top to bottom so as soon as it comes across a input with the required attribute that's input is empty it stops checking and displays the error message on that input. So if a user had two blank required fields the next error would not be displayed until they correct the first and hit the submit button again. But what if we wanted to turn off validation? This can easily done with the attribute `novalidate`. Someone might do this if they wanted to test server side code.

### CSS Styling for Validation

In the previous section we were introduced the required attribute. This section will introduce a few new attributes to you. `valid` and `invalid` which apply styles to elements if they contain mistakes. However the HTML form does not actually know there is a mistake until the submit button is hit. An example of CSS styling form elements is.
`input:required {`  
 `background-color: yellow;`  
`}`
We can also style items after the submit button has been hit on a invalid item like..
`input:required:invalid {`  
 `background-color: yellow;`  
`}`

### Regular Expressions

A regular expression is a pattern written in the regular expression language. The regular expression language can do things like make sure an email contains the @ symbol or that a postal code follows the correct sequence of digits and numbers. Check out this example below..

`[0-9]{3}-[A-Z]{3}`

What does this expression mean? The square brackets `[0-9]` only accepts digits ranging from 0-9 the `{3}` means that 3 digits between 0-9 are required. The `[A-Z]` means only capital letters from A-Z are acceptable and the `{3}` means there must be 3 of them.

`587-ADC` -- This would be an acceptable combo
`587-Adc` -- This would not be

More information on regular expressions [here](https://www.w3schools.com/jsref/jsref_obj_regexp.asp)
