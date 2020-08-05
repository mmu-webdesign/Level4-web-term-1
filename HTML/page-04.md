# Nesting, Block and Inline elements

## Nesting elements

Elements can be placed within other elements. This is called nesting. If we wanted to state that our cat is very grumpy, we could wrap the word very in a `<strong>` element, which means that the word is to have strong(er) text formatting:

```
<p>My cat is <strong>very</strong> grumpy.</p>
```

There is a right and wrong way to do nesting. In the example above, we opened the p element first, then opened the strong element. For proper nesting, we should close the strong element first, before closing the p.

The following is an example of the wrong way to do nesting:

```
<p>My cat is <strong>very grumpy.</p></strong>
```

The tags have to open and close in a way that they are inside or outside one another. With the kind of overlap in the example above, the browser has to guess at your intent. This kind of guessing can result in unexpected results.

> The nesting rule is **first in, last out**.

## Block versus inline elements

There are two important categories of elements to know in HTML: block-level elements and inline elements.

- **Block-level elements** form a visible block on a page. A block-level element appears on a new line following the content that precedes it. Any content that follows a block-level element also appears on a new line. Block-level elements are usually structural elements on the page. For example, a block-level element might represent headings, paragraphs, lists, navigation menus, or footers. A block-level element wouldn't be nested inside an inline element, but it might be nested inside another block-level element.

- **Inline elements** are contained within block-level elements, and surround only small parts of the document’s content. (not entire paragraphs or groupings of content) An inline element will not cause a new line to appear in the document. It is typically used with text. For example, as an `<a>` element (hyperlink) or emphasis elements such as `<em>` or `<strong>`.

Consider the following example:

```
<em>first</em><em>second</em><em>third</em>

<p>fourth</p><p>fifth</p><p>sixth</p>
```

`<em>` is an inline element. As you see below, the first three elements sit on the same line, with no space in between. On the other hand, `<p>` is a block-level element. Each p element appears on a new line, with space above and below. (The spacing is due to default CSS styling that the browser applies to paragraphs.)

<em>first</em><em>second</em><em>third</em>

<p>fourth</p><p>fifth</p><p>sixth</p>

> Note: Find useful [MDN reference pages](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference) that include lists of block and inline elements. See [Block-level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) and [Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements).

## Empty elements

Not all elements follow the pattern of an opening tag, content, and a closing tag. Some elements consist of a single tag, which is typically used to insert/embed something in the document. For example, the `<hr>` element draws a line onto a page:

<hr> 

Some of the more seasoned coders (like Derren) will remember the self closing version of this element from XHTML.

`<hr />` - we don't need to do this anymore in html5.

We will shortly be introducing the image element, `<img>` which is also self closing and one element you will be using frequently.

<div class="deep">

## Deeper Learning
To get a better understanding of this topic use the following resources.

- MDN: `<hr>` - [The Thematic Break (Horizontal Rule) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)

</div>


### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).