# Lang attribute, Div, Span, br and hr

## Lang attribute

The `lang` attribute is a global attribute. These are attributes common to all HTML elements; they can be used on all elements, though they may have no effect on some elements.

`Lang` is used to define the language used within a particular element. You will see that we can set the global language of a document, but using the `lang` attribute lets us target a specific sentence, block or phrase.

As an example:

```
<p>This paragraph is English, but the language is not specifically defined.</p>

<p lang="en-GB">This paragraph is defined as British English.</p>

<p lang="fr">Ce paragraphe est défini en français.</p>

```
The `en-GB` attribute defines the language used as British as opposed to the default `lang="en"` which is USA.

The `lang="fr"` ensures that a screen reader or AI voice will read that particular sentence in French, as opposed to continuing reading it as English.

These language codes are defined by the [ISO 639-1 standard](https://en.wikipedia.org/wiki/ISO_639-1). 


## Non-semantic wrappers

Sometimes you'll come across a situation where you can't find an ideal semantic element to group some items together or wrap some content. Sometimes you might want to just group a set of elements together to affect them all as a single entity with some CSS or JavaScript. For cases like these, HTML provides the `<div>` and `<span>` elements. You should use these preferably with a suitable class attribute, to provide some kind of label for them so they can be easily targeted.

`<span>` is an inline non-semantic element, which you should only use if you can't think of a better semantic text element to wrap your content, or don't want to add any specific meaning. For example:

```
<p>The King walked drunkenly back to his room at 01:00, the beer doing nothing to aid
him as he staggered through the door <span class="editor-note">[Editor's note: At this point in the
play, the lights should be down low]</span>.</p>

```

In this case, the editor's note is supposed to merely provide extra direction for the director of the play; it is not supposed to have extra semantic meaning. For sighted users, CSS would perhaps be used to distance the note slightly from the main text.

`<div>` is a block level non-semantic element, which you should only use if you can't think of a better semantic block element to use, or don't want to add any specific meaning. For example, imagine a shopping cart widget that you could choose to pull up at any point during your time on an e-commerce site:

```
<div class="shopping-cart">
  <h2>Shopping cart</h2>
  <ul>
    <li>
      <p><a href=""><strong>Silver earrings</strong></a>: $99.95.</p>
      <img src="../products/3333-0985/thumb.png" alt="Silver earrings">
    </li>
    <li>
      ...
    </li>
  </ul>
  <p>Total cost: $237.89</p>
</div>

```

This isn't really an `<aside>`, as it doesn't necessarily relate to the main content of the page (you want it viewable from anywhere). It doesn't even particularly warrant using a  `<section>`, as it isn't part of the main content of the page. So a `<div>` is fine in this case. We've included a heading as a signpost to aid screenreader users in finding it.

<div class="warning">

Warning: Divs are so convenient to use that it's easy to use them too much. As they carry no semantic value, they just clutter your HTML code. Take care to use them only when there is no better semantic solution and try to reduce their usage to the minimum otherwise you'll have a hard time updating and maintaining your documents.
</div>

## Line breaks

`<br>` creates a line break in a paragraph; it is the only way to force a rigid structure in a situation where you want a series of fixed short lines, such as in a postal address or a poem. For example:

```
There once was a man named O'Dell<br>
Who loved to write HTML<br>
But his structure was bad, his semantics were sad<br>
and his markup didn't read very well.
```

Without the `<br>` elements, the paragraph would just be rendered in one long line (as we said earlier in the course, HTML ignores most whitespace); with `<br> `elements in the code, the markup renders like this:

<div class="output">

There once was a man named O'Dell<br>
Who loved to write HTML<br>
But his structure was bad, his semantics were sad<br>
and his markup didn't read very well.

</div>

<div class="warning">

DO NOT use the `<br>` element to either create the illusion of paragraph breaks or to create space on the page. For the former always the `<p>` element, for the latter, use CSS to add space with padding and margins.

</div>

## Horizontal rule

`<hr>` elements create a horizontal rule in the document that denotes a thematic change in the text (such as a change in topic or scene). Visually it just looks like a horizontal line. As an example:

```
<p>Ron was backed into a corner by the marauding netherbeasts. Scared, but determined to protect his friends, he raised his wand and prepared to do battle, hoping that his distress call had made it through.</p>
<hr>
<p>Meanwhile, Harry was sitting at home, staring at his royalty statement and pondering when the next spin off series would come out, when an enchanted distress letter flew through his window and landed in his lap. He read it hazily and sighed; "better get back to work then", he mused.</p>
```

Would render like this:

<div class="output">

<p>Ron was backed into a corner by the marauding netherbeasts. Scared, but determined to protect his friends, he raised his wand and prepared to do battle, hoping that his distress call had made it through.</p>
<hr>
<p>Meanwhile, Harry was sitting at home, staring at his royalty statement and pondering when the next spin off series would come out, when an enchanted distress letter flew through his window and landed in his lap. He read it hazily and sighed; "better get back to work then", he mused.</p>

</div>

<div class="deep">

## Deeper Learning
To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons - Supporting langauges](https://www.linkedin.com/learning/html-essential-training-4/supporting-languages?u=36102708) (4m 6s)

- MDN: `lang` - [The Lang attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang)

- LinkedIn Learning Video: [Jen Simmons - Div and span](https://www.linkedin.com/learning/html-essential-training-4/generic-elements-div-and-span?u=36102708) (4m 12s)

- MDN: `<div>` - [The Content Division element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div)

- MDN: `<span>` - [The Span element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span)

- MDN: `<br>` - [The Line Break element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)

- MDN: `<hr>` - [The Thematic Break (Horizontal Rule) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)

</div>

### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).



