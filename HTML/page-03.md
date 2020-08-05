
# Emphasis and importance

This topic gets very confusing, very quickly. Watch Jen's video for a clear explanation before you start. 

- LinkedIn Learning Video: [Jen Simmons - Bold and Italics](https://www.linkedin.com/learning/html-essential-training-4/bold-and-italics?u=36102708) 4m 55s

In human language, we often *emphasise* certain words to alter the meaning of a sentence, and we often want to mark certain words as important or different in some way. HTML provides various semantic elements to allow us to mark up textual content with such effects, and in this section, we'll look at a few of the most common ones.

## Emphasis

When we want to add emphasis in spoken language, we stress certain words, subtly altering the meaning of what we are saying. Similarly, in written language we tend to stress words by putting them in italics. For example, the following two sentences have different meanings.

I am glad you weren't late.

I am *glad* you weren't late.

The first sentence sounds genuinely relieved that the person wasn't late. In contrast, the second one sounds sarcastic or passive-aggressive, expressing annoyance that the person arrived a bit late (because the emphasis is on the word *glad*).

In HTML we use the `<em>` (emphasis) element to mark up such instances. As well as making the document more interesting to read, these are recognised by screen readers and spoken out in a different tone of voice. Browsers style this as italic by default, but you shouldn't use this tag purely to get italic styling. To do that, you'd use a `<span>` element and some CSS, or perhaps an `<i>` element (see below).

```
<p>I am <em>glad</em> you weren't <em>late</em>.</p>
```

## Strong importance

To emphasize important words, we tend to stress them in spoken language and bold them in written language. For example:

This liquid is **highly toxic**.

I am counting on you. **Do not** be late!

In HTML we use the `<strong>` (strong importance) element to mark up such instances. As well as making the document more useful, again these are recognized by screen readers and spoken in a different tone of voice. Browsers style this as bold text by default, but you shouldn't use this tag purely to get bold styling. To do that, you'd use a `<span>` element and some CSS, or perhaps a `<b>` element (see below).

```
<p>This liquid is <strong>highly toxic</strong>.</p>

<p>I am counting on you. <strong>Do not</strong> be late!</p>
```

You can nest strong and emphasis inside one another if desired:

```
<p>This liquid is <strong>highly toxic</strong> —
if you drink it, <strong>you may <em>die</em></strong>.</p>
```

## Italic, bold, underline...


The elements we've discussed so far have clearcut associated semantics. The situation with `<b>`, `<i>`, and `<u>` is somewhat more complicated. They came about so people could write bold, italics, or underlined text in an era when CSS was still supported poorly or not at all. Elements like this, which only affect presentation and not semantics, are known as presentational elements and should no longer be used, because as we've seen before, semantics is so important to accessibility, SEO, etc.

HTML5 redefined `<b>`, `<i>` and `<u>` with new, somewhat confusing, semantic roles.

Here's the best rule of thumb: it's likely appropriate to use `<b>`, `<i>`, or `<u>` to convey a meaning traditionally conveyed with bold, italics, or underline, provided there is no more suitable element. However, it always remains critical to keep an accessibility mindset. The concept of italics isn't very helpful to people using screen readers, or to people using a writing system other than the Latin alphabet.

- `<i>` is used to convey a meaning traditionally conveyed by italic: Foreign words, taxonomic designation, technical terms, a thought...
- `<b>` is used to convey a meaning traditionally conveyed by bold: Key words, product names, lead sentence...
- `<u>` is used to convey a meaning traditionally conveyed by underline: Proper name, misspelling...

>A kind warning about underline: People strongly associate underlining with hyperlinks. Therefore, on the Web, it's best to underline only links. Use the `<u>` element when it's semantically appropriate, but consider using CSS to change the default underline to something more appropriate on the Web. The example below illustrates how it can be done.


### Example - scientific names
```
<p>
  The Ruby-throated Hummingbird (<i>Archilochus colubris</i>)
  is the most common hummingbird in Eastern North America.
</p>
```

### Example - foreign words
```
<p>
  The menu was a sea of exotic words like <i lang="uk-latn">vatrushka</i>,
  <i lang="id">nasi goreng</i> and <i lang="fr">soupe à l'oignon</i>.
</p>
```

### Example - a known misspelling
```
<p>
  Someday I'll learn how to <u style="text-decoration-line: underline; text-decoration-style: wavy;">spel</u> better.
</p>
```

### Example - Highlight keywords in a set of instructions
```
<ol>
  <li>
    <b>Slice</b> two pieces of bread off the loaf.
  </li>
  <li>
    <b>Insert</b> a tomato slice and a leaf of
    lettuce between the slices of bread.
  </li>
</ol>
```
<div class="deep">

## Deeper Learning
To get a better understanding of this topic use the following resources.

- MDN: `<em>` - [The Emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)

- MDN: `<strong>` - [The Strong element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)

- MDN: `<i>` - [The Idiomatic Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)

- MDN: `<b>` - [The Bring To Attention element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)

- MDN: `<u>` - [The Unarticulated Annotation (Underline) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u)

</div>

### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).
