# Introduction to CSS

## What is CSS for?

CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

A document is usually a text file structured using a markup language — `HTML` is the most common markup language, but you may also come across other markup languages such as `SVG` or `XML`.

Presenting a document to a user means converting it into a form usable by your audience. Browsers, like Firefox, Chrome, or Edge , are designed to present documents visually, for example, on your laptop, tablet or mobile.

> Note: A browser is sometimes called a `user agent`, which basically means a computer program that represents a person inside a computer system. Browsers are the main type of `user agent` we think of when talking about CSS, however, it is not the only one. There are other `user agent`s available — such as those which convert HTML and CSS documents into PDFs to be printed.

CSS can be used for very basic document text styling — for example changing the color and size of headings and links. It can be used to create layout — for example turning a single column of text into a layout with a main content area and a sidebar for related information. It can even be used for effects such as animation. Have a look at the links in this paragraph for specific examples.

## Browser default styles

In the HTML books we covered what HTML is, and how it is used to mark up documents. These documents will be readable in a web browser. Headings will look larger than regular text, paragraphs break onto a new line and have space between them. Links are colored and underlined to distinguish them from the rest of the text. What you are seeing is the browser's default styles — very basic styles that the browser applies to HTML to make sure it will be basically readable even if no explicit styling is specified by the author of the page.

However, the web would be a boring place if all websites looked like that. Using CSS you can control exactly how HTML elements look in the browser, presenting your markup using whatever design you like.

<figure>
<img src="media/mmu-no-css.png">
<figcaption>
Like most large websites, if you remove the custom styles and revert to the browser default styles all you get is a vast list of links and a few images.
</figcaption>
</figure>

## Browser developer tools

The developer tools (Dev Tools) in your browser can really help understand and bug test your CSS. It also helps you understand the User Agent Styles that the browser is applying.

<!-- div class="exercise" -->
## Exercise One

> How to use browser developer tools

### Task 1

- Watch this video to get a good understanding of how the Dev Tools work, and how to see both browser styles and your own. You can [view the sample file](media/example.html) in your browser and follow the task demonstrated.

- LinkedIn Learning Video: [Browser developer tools](https://www.linkedin.com/learning-login/share?forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Fcss-essential-training-3%3Ftrk%3Dshare_ent_url&account=36102708) - Every modern browser includes a set of browser developer tools, which can be used to inspect the HTML, CSS and JavaScript on any webpage.

<!-- end div -->

## Anatomy of a CSS ruleset

Let's dissect the CSS code for red paragraph text to understand how it works :

<img src="media/css-declaration-small.png" alt="CSS p declaration color red">


The whole structure is called a ruleset. (The term ruleset is often referred to as just rule, a CSS rule.) Note the names of the individual parts:

### Selector
This is the HTML element name at the start of the ruleset. It defines the element(s) to be styled (in this example, <p> elements). To style a different element, change the selector.

### Declaration
This is a single rule like color: red;. It specifies which of the element's properties you want to style.

### Properties
These are ways in which you can style an HTML element. (In this example, color is a property of the `<p>` elements.) In CSS, you choose which properties you want to affect in the rule.

### Property value
To the right of the property—after the colon—there is the property value. This chooses one out of many possible appearances for a given property. (For example, there are many color values in addition to red.)

Note the other important parts of the syntax:

- Apart from the selector, each ruleset must be wrapped in curly braces. (`{ }`)
- Within each declaration, you must use a colon (`:`) to separate the property from its value or values.
- Within each ruleset, you must use a semicolon (`;`) to separate each declaration from the next one.
- To modify multiple property values in one ruleset, write them separated by semicolons, like this:

```
p {
  color: red;
  width: 400px;
  border: 1px solid black;
}
```

<!-- div class="exercise" -->
## Exercise Two

> Apply this simple CSS ruleset

### Task 1

- Open the exercise files in another browser window - [Repl.it - First CSS](https://repl.it/@webdesignmmu/css01) 

- Run the page in the browser to see the heading and paragraphs.

- Note that browser default (User Agent) styles include larger font size for the `<h1>`, margins above and below the heading and paragraphs; and margins to the left and right.

### Task 2

- Apply our own styles.

- Select the `style.css` file in the editor - it should be blank

- Copy & paste our initial style into `style.css`

```
p {
  color: red;
  width: 400px;
  border: 1px solid black;
}
```
- Select `index.html` and Run the page to view it in the browser.

- You should now have a page like this:

<figure>
<img src="media/css01.png" alt="The page rendered in the browser, each paragraph with red text, a width of 400px and a thin black border">
<figcaption>
It doesn't look pretty, but you have applied three styles to all paragraphs on the page.
</figcaption>
</figure>

- Read through the CSS ruleset and identify the styles.

```
p {
  color: red;
  width: 400px;
  border: 1px solid black;
}
```

- In plain english the ruleset reads:

    + Every paragraph on the page
    + font colour red (notice the USA spelling)
    + each paragraph is 400 pixel wide
    + each paragraph gets a 1 pixel wide, solid (not dotted or dashed) border, colour black.

### Task 2

- To finish off, try to add a further ruleset that  targets the `<h1>` heading, to make the text blue.

- The **selector** is the **element** - the `<h1>`, followed by the curly brackets. Add this under the current ruleset to `style.css`:

```
h1 {

}
```
- Next is the Declaration, which sits between the curly brackets. Remember it is **property** `colon` **value** `semi-colon`.

```
h1 {
property: value;
}
```
- Your property is the colour (spelt `color`) and the value is `blue`.

- Complete the style and Run `index.html` in the browser.

<figure>
<img src="media/blue-heading.png" alt="The page rendered in the browser, now with a blue heading">
<figcaption>
Is your heading blue?
</figcaption>
</figure>

<!-- end div -->

> How have we applied these styles? We will talk about that next.

<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- Mozilla Developer Video: [Where do browser styles come from](https://youtu.be/spK_S0HfzFw) (7m 01s) - More detail.

- MDN: `<p>` - [The Paragraph element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)

- LinkedIn Learning Video: [Jen Simmons -  Formatting html](https://www.linkedin.com/learning/html-essential-training-4/formatting-html?u=36102708) (4m 30s)

<h2 class="books">CSS Resources</h2>

- THE resource for all things CSS - [CSS Tricks](https://css-tricks.com/)

- LinkedIn Learning Video - The full [CSS Essential Training](https://www.linkedin.com/learning/css-essential-training-3/)


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).