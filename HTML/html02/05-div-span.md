# Non-semantic wrappers

Sometimes you'll come across a situation where you can't find an ideal semantic element to group some items together or wrap some content. Sometimes you might want to just group a set of elements together to affect them all as a single entity with some CSS or JavaScript. For cases like these, HTML provides the `<div>` and `<span>` elements. You should use these preferably with a suitable class attribute, to provide some kind of label for them so they can be easily targeted.

## The `<span>` element

`<span>` is an inline non-semantic element, which you should only use if you can't think of a better semantic text element to wrap your content, or don't want to add any specific meaning. For example:

```
<p>The King walked drunkenly back to his room at 01:00, the beer doing nothing to aid
him as he staggered through the door <span class="editor-note">[Editor's note: At this point in the play, the lights should be down low]</span>.</p>

```

In this case, the editor's note is supposed to merely provide extra direction for the director of the play; it is not supposed to have extra semantic meaning. For sighted users, CSS would perhaps be used to distance the note slightly from the main text.

### `<span>` - thing to remember

- `<span>` is an inline element, it can for example be used mid paragraph without disrupting the text.

- `<span>` is non-semantic, it carries no meaning - it does not describe the type of content it contains.

- Mostly it is used on conjunction with CSS to apply a style to something.



## The `<div>` element

`<div>` is a block level non-semantic element, which you should only use if you can't think of a better semantic block element to use, or don't want to add any specific meaning. For example, imagine a shopping cart widget that you could choose to pull up at any point during your time on an e-commerce site:

```
<div class="shopping-cart">
  <h2>Shopping cart</h2>
  <ul>
    <li>
      USB C Cable 3m £25
    </li>
    <li>
      USB C charger £75
    </li>
  </ul>
  <p>Total cost: £100</p>
</div>

```

A `<div>` works fine in this case to group the content. We've included a heading as a signpost to aid screenreader users in finding it.

### `<div>` - thing to remember

- `<div>` is a block element. Like other block elements such as `<p>` and `<ul>`, it creates its own space on the page. 

- It can contain other block elements as per our example above.

- `<div>` is non-semantic, it carries no meaning - it does not describe the type of content it contains.

- Mostly it is used in conjunction with CSS to apply a style to something.

- Previously `<div>` was used to define the stucture of a web page using classes or IDs (more to come on these in CSS) to name each section. For example:

```
<body>
<div class="header">
    Header... 
</div>

<div class="nav">
    Navigation... 
</div>

<div class="content">
    Main content...
</div>

<div class="footer">
    Page footer... 
</div>
</body>
```

- This is now a dated approach and we will be looking at the semantic solution later.

<h3 class="warning">Divitus - the over use of divs</h3>

**Warning**: Divs are so convenient to use that it's easy to use them too much. As they carry no semantic value, they just clutter your HTML code. Take care to use them only when there is no better semantic solution and try to reduce their usage to the minimum otherwise you'll have a hard time updating and maintaining your documents.

<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons - Div and span](https://www.linkedin.com/learning/html-essential-training-4/generic-elements-div-and-span?u=36102708) (4m 12s)

- MDN: `<div>` - [The Content Division element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div)

- MDN: `<span>` - [The Span element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span)


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).
