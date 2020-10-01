# Introduction to CSS layout

CSS page layout techniques allow us to take elements contained in a web page and control where they are positioned relative to their default position in normal layout flow, the other elements around them, their parent container, or the main viewport/window.  This chapter gives a brief overview of each page layout technique:

- Normal flow
- The [display](https://developer.mozilla.org/en-US/docs/Web/CSS/display) property
- Flexbox
- Grid
- Floats
- Positioning
- Table layout
- Multiple-column layout

Each technique has its uses, advantages, and disadvantages, and no technique is designed to be used in isolation. By understanding what each method is designed for you will be in a good place to understand which is the best layout tool for each task.

In the second assignment we will be making full use of Flexbox and coving this in more detail.

> Advanced students may want to undertake the full [MDN CSS layout tutorial](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout) written by Rachel Andrew, to gain a deeper understanding. **It is not necessary to successfully complete the two assignments**.

## Normal flow

Normal flow is how the browser lays out HTML pages by default when you do nothing to control page layout. Let's look at a quick HTML example:

```
<p>I love my cat.</p>
    
<ul>
  <li>Buy cat food</li>
  <li>Exercise</li>
  <li>Cheer up friend</li>
</ul>
    
<p>The end!</p>
```

By default, the browser will display this code as follows:

<p>I love my cat.</p>
    
<ul>
  <li>Buy cat food</li>
  <li>Exercise</li>
  <li>Cheer up friend</li>
</ul>
    
<p>The end!</p>

Note here how the HTML is displayed in the exact order in which it appears in the source code, with elements stacked up on top of one another — the first paragraph, followed by the unordered list, followed by the second paragraph.

The elements that appear one below the other are described as block elements, in contrast to inline elements, which appear one beside the other, like the individual words in a paragraph.

> Note: The direction in which block element contents are laid out is described as the Block Direction. The Block Direction runs vertically in a language such as English, which has a horizontal writing mode. It would run horizontally in any language with a Vertical Writing Mode, such as Japanese. The corresponding Inline Direction is the direction in which inline contents (such as a sentence) would run.

For many of the elements on your page the normal flow will create exactly the layout you need, however for more complex layouts you will need to alter this default behavior using some of the tools available to you in CSS. Starting with a well-structured HTML document is very important, as you can then work with the way things are laid out by default rather than fighting against it.

The methods that can change how elements are laid out in CSS are as follows:

- **The display property** — Standard values such as `block`, `inline` or `inline-block` can change how elements behave in normal flow, for example making a block-level element behave like an inline element. We also have entire layout methods that are switched on via specific display values, for example `CSS Grid` and `Flexbox`, which alter how elements inside the element they are set on are laid out.

- **Floats** — Applying a float value such as left can cause block level elements to wrap alongside one side of an element, like the way images sometimes have text floating around them in magazine layouts.

- **The position property** — Allows you to precisely control the placement of boxes inside other boxes. static positioning is the default in normal flow, but you can cause elements to be laid out differently using other values, for example always fixed to the top of the browser viewport.

- **Table layout** — features designed for styling the parts of an HTML table can be used on non-table elements using `display: table` and associated properties.

- **Multi-column layout** — The Multi-column layout properties can cause the content of a block to layout in columns, as you might see in a newspaper.

<!-- div class="exercise" -->
## ToDo 

> Basic document flow.

### Task 1 

- Open the `css15` folder in Visual Studio Code.

- Open `example-a.html` in your editor and look over the code.

    + A heading.

    + 4 paragraphs.

    + 4 inline elements - 3 x `<span>` and 1 x `<img>`.

- Open `example-a.html` in your browser.

<figure>
<img src="media/ex-15-1.png" alt="The basic flow example">
<figcaption>
Read through the text as it explains clearly the normal flow of each element.
</figcaption>
</figure>

- The example files are not part of the assessment.

- You can leave them in the folder.

<!-- end div -->

## The display property

The main methods of achieving page layout in CSS are all values of the display property. This property allows us to change the default way something displays. Everything in normal flow has a value of display, used as the default way that elements they are set on behave. For example, the fact that paragraphs in English display one below the other is due to the fact that they are styled with display: block. If you create a link around some text inside a paragraph, that link remains inline with the rest of the text, and doesn’t break onto a new line. This is because the `<a>` element is display: inline by default.

You can change this default display behavior. For example, the `<li>` element is display: block by default, meaning that list items display one below the other in our English document. If we change the display value to inline they now display next to each other, as words would do in a sentence. The fact that you can change the value of display for any element means that you can pick HTML elements for their semantic meaning, without being concerned about how they will look. The way they look is something that you can change.

In addition to being able to change the default presentation by turning an item from block to inline and vice versa, there are some bigger layout methods that start out as a value of display. However, when using these, you will generally need to invoke additional properties. The two values most important for our purposes when discussing layout are `display: flex` and `display: grid`.


## Flexbox

Flexbox is the short name for the [Flexible Box Layout Module](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout), designed to make it easy for us to lay things out in one dimension — either as a row or as a column. To use flexbox, you apply `display: flex` to the parent element of the elements you want to lay out; all its direct children then become flex items. We can see this in a simple example.

<!-- div class="exercise" -->
## Exercise 15a 

> Flexbox.

### Task 1

- Return to the `css15` folder in Visual Studio Code.

- Open `exercise-15a.html` in your editor and look over the code.

- Open `exercise-15a.html` in your browser.

<figure>
<img src="media/ex-15-2.png" alt="The flexbox example">
<figcaption>
The HTML markup gives us a containing element (<code>&lt;div&gt;</code>), with a class of <code>wrapper</code>, inside which are three <code>&lt;div&gt;</code> elements. By default these would display as block elements, below one another, in our English language document.
</figcaption>
</figure>

- By adding `display: flex` to the parent, the three items now arrange themselves into columns. This is due to them becoming flex items and being affected by some initial values that flexbox sets on the flex container. They are displayed in a row, because the initial value of [flex-direction](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction) set on their parent is `row`. They all appear to stretch to the height of the tallest item, because the initial value of the [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items) property set on their parent is `stretch`. This means that the items stretch to the height of the flex container, which in this case is defined by the tallest item. The items all line up at the start of the container, leaving any extra space at the end of the row.

### Task 2

- Return to `exercise-15a.html` in the editor.

- Remove the style rule `display: flex;`.

```
    .wrapper {

    }
```

- Save `exercise-15a.html` and refresh it in your browser.

<figure>
<img src="media/ex-15-3.png" alt="Minus flexbox example">
<figcaption>
The <code>&lt;div&gt;</code>'s now sit in their normal flow, one on top of the other.
</figcaption>
</figure>

### Task 3

- Return to `exercise-15a.html` in the editor.

- Reapply the style rule `display: flex;` to the class `.wrapper`.

```
    .wrapper {
        display: flex;
    }
```

- Save `exercise-15a.html` and refresh it in your browser and check that Flexbox has been re-applied.

### Task 4

- In addition to the above properties that can be applied to the flex container, there are properties that can be applied to the flex items. These properties, among other things, can change the way that the items flex, enabling them to expand and contract to fit into the available space.

- As a simple example of this, we can add the [flex property](https://developer.mozilla.org/en-US/docs/Web/CSS/flex) to all of our child items, with a value of `1`. This will cause all of the items to grow and fill the container, rather than leaving space at the end. If there is more space then the items will become wider; if there is less space they will become narrower. In addition, if you add another element to the markup the items will all become smaller to make space for it — they will adjust size to take up the same amount of space, whatever that is.

- Let's try this out.

- Return to `exercise-15a.html` in the editor.

- To see this work a little easier we want you to reduce the sizes of the paragraphs.

```
        <div class="box1">    
            <p>Cray food truck.</p>
        </div>

        <div class="box2">    
            <p>Cray food truck.</p>
        </div>
        
        <div class="box3">    
            <p>Cray food truck.</p>
        </div>
```
- Save `exercise-15a.html` and refresh it in your browser. 

<figure>
<img src="media/ex-15-4.png" alt="Smaller flexboxes">
<figcaption>
We still have three flexboxes, but they are now much smaller. This will make the next demonstration clearer.
</figcaption>
</figure>

- Return to `exercise-15a.html` in the editor.

- Apply the following style to the bottom of your existing styles:

```
    .wrapper > div {
    flex: 1;
    }
```
- Save `exercise-15a.html` and refresh it in your browser. 

<figure>
<img src="media/ex-15-5.png" alt="Smaller flexboxes">
<figcaption>
Our three flexboxes, all with the flex value of 1, take up equal space across the page.
</figcaption>
</figure>

- Return to `exercise-15a.html` in the editor.

- Add another box, `box4` inside your `wrapper` div.

```
        <div class="box4">    
            <p>Cray food truck.</p>
        </div>
```
- Save `exercise-15a.html` and refresh it in your browser. 

<figure>
<img src="media/ex-15-6.png" alt="Smaller flexboxes">
<figcaption>
Our four flexboxes, all with the flex value of 1, take up equal space across the page. The extra box is accomodated with ease.
</figcaption>
</figure>

- To someone new to web development this all seems fairly obvious that you can lay out 4 boxes across the page, evenly.

- To anyone dealing with CSS for a number of years, this seems like a modern miracle - a fix for something that had previously been painful to achieve.

<!-- end div -->

> Note: This has been a very short introduction to what is possible in Flexbox. We will be doing more in the second assignment. Those keen to find out more, see the [MDN Flexbox article](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox).




