# Styling Lists and Links

## Styling lists

Lists behave like any other text for the most part, but there are some CSS properties specific to lists that you need to know about, and some best practices to consider.

To begin with, let's look at a simple list example. Throughout this chapter, we'll look at unordered, ordered, and description lists — all have styling features that are similar, and some that are particular to their type of list. 

<!-- div class="exercise" -->
## Exercise 8

> A simple list example

### Task 1

- Open the `css08` folder.

- Open `exercise-08.html` in your editor.

<figure>
<img src="media/ex-08.png" alt="The VSC interface">
<figcaption>
The Visual Studio Code (VSC) editor window.
</figcaption>
</figure>

### Task 2

- Open `exercise-08.html` in the browser to check it works.

<figure>
<img src="media/ex-08-1.png" alt="exercise-08.html rendered in the browser">
<figcaption>
The page with the browser default styles.
</figcaption>
</figure>

- Each list has default User Agent (Browser) styles applied including margins and padding to create space and indents.

- If you can, investigate the list elements User Agent (browser) default styles using browser developer tools.


### Task 3

- Open `style.css` in the editor.

- Copy and paste these styles and comments into the empty `style.css`: 

```
/* General styles */

html {
  font-family: Helvetica, Arial, sans-serif;
  font-size: 10px;
}

h2 {
  font-size: 2rem;
}

ul,ol,dl,p {
  font-size: 1.5rem;
}

li, p {
  line-height: 1.5;
}

/* Description list styles */


dd, dt {
  line-height: 1.5;
}

dt {
  font-weight: bold;
}
```

- Save `style.css` and refresh `exercise-08.html` in the browser.

<figure>
<img src="media/ex-08-2.png" alt="exercise-08.html rendered in the browser">
<figcaption>
The page now looks a little sharper with styles applied.
</figcaption>
</figure>

### Task 4

#### Let's review each of the styles applied:

- The first rule sets a sitewide font and a baseline font size of 10px. These are inherited by everything on the page.

- Rules 2 and 3 set relative font sizes for the headings, different list types (the children of the list elements inherit these), and paragraphs. This means that each paragraph and list will have the same font size and top and bottom spacing, helping to keep the vertical rhythm consistent.

- Rule 4 sets the same line-height on the paragraphs and list items — so the paragraphs and each individual list item will have the same spacing between lines. This will also help to keep the vertical rhythm consistent.

- Rules 5 and 6 apply to the description list — we set the same line-height on the description list terms and descriptions as we did with the paragraphs and list items. Again, consistency is good! We also make the description terms have bold font, so they visually stand out easier.

<!-- end div -->

## List-specific styles

Now we've looked at general spacing techniques for lists, let's explore some list-specific properties. There are three properties you should know about to start with, which can be set on `<ul>` or `<ol>` elements:

- [list-style-type](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type): Sets the type of bullets to use for the list, for example, square or circle bullets for an unordered list, or numbers, letters or roman numerals for an ordered list.

- [list-style-position](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position): Sets whether the bullets appear inside the list items, or outside them before the start of each item.

- [list-style-image](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-image): Allows you to use a custom image for the bullet, rather than a simple square or circle.

<!-- div class="exercise" -->
## Exercise 8 continued

> Bullet styles

- As mentioned above, the list-style-type property allows you to set what type of bullet to use for the bullet points. 

- Return to `style.css` in the editor.

- Set the ordered list to use uppercase roman numerals by adding the following style and comment at the bottom of `style.css`:

```
/* Additional styles */

ol {
list-style-type: upper-roman;
}
```
- Save `style.css` and refresh `exercise-08.html` in the browser.

<figure>
<img src="media/ex-08-3.png" alt="exercise-08.html rendered in the browser">
<figcaption>
If successful, your list style has changed to uppercase roman numerals.
</figcaption>
</figure>

> Bullet position

The list-style-position property sets whether the bullets appear inside the list items, or outside them before the start of each item. The default value is outside, which causes the bullets to sit outside the list items, as seen above.

If you set the value to inside, the bullets will sit inside the lines: