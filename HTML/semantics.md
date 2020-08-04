# Semantics

Before starting watch the following short video introduction:

> LinkedIn Learning Video: Jen Kramer [Craft meaningful html](https://www.linkedin.com/learning/crafting-meaningful-html/craft-meaningful-html?u=36102708) 1m 49s

Our teaching philosophy is pretty much the same as Jen's as you will hear us talking about semantic mark-up a lot. As she says, '*the hypertext markup language is about identifying the types of content on a webpage*'.

In HTML, for example, the `<h1>` element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

```
<h1>This is a top level heading</h1>
```

By default, most browser's user agent stylesheet will style an `<h1>` with a large font size to make it look like a heading (although you could style it to look like anything you wanted - see above *Visuals*).

On the other hand, you could make any element look like a top level heading. The following styles (CCS - to follow) adjusts a paragraph so it would display the same as the default (larger) heading styles.

```
<span style="font-size: 32px; margin: 21px 0;">Is this a top level heading?</span>
```

This will render it to look like a top level heading, but it has no semantic value, so it will not get any extra benefits as described above. It is therefore a good idea to use the right HTML element for the right job.

> This is actually semantic HTML in a nutshell - *use the right HTML element for the right job*.

HTML should be coded to represent the data that will be populated and not based on its default presentation styling. Presentation (how it should look), is the sole responsibility of CSS.

Some of the benefits from writing semantic markup are as follows:

- Search engines will consider its contents as important keywords to influence the page's search rankings (see SEO)
- Screen readers can use it as a signpost to help visually impaired users navigate a page
- Finding blocks of meaningful code is significantly easier than searching though endless divs with or without semantic or namespaced classes
- Suggests to the developer the type of data that will be populated
- Semantic naming mirrors proper custom element/component naming

When approaching which markup to use, ask yourself, "What element(s) best describe/represent the data that I'm going to populate?" For example, is it a list of data?; ordered, unordered?; is it an article with sections and an aside of related information?; does it list out definitions?; is it a figure or image that needs a caption?; should it have a header and a footer in addition to the global site-wide header and footer?; etc.

## Deeper Learning
To get a better understanding of this topic use the following resources.

> Article: Paul Boag - [Semantic code: What? Why? How?](https://boagworld.com/dev/semantic-code-what-why-how/)

> MDN: [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)

## Advanced Learning
For students wanting more, we recommend the following topics and resources. 

Students who already have a knowledge of html may want to complete the full course on crafting meaningful html. In our experience the area of semantics is something that many self taught coders, and even current professionals ignore.

> LinkedIn Learning Video: Jen Kramer - [Craft meaningful html](https://www.linkedin.com/learning/crafting-meaningful-html/craft-meaningful-html?u=36102708) 1hr 22m


### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).