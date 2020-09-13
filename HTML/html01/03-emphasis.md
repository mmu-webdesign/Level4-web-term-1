
# Emphasis and importance

This topic gets very confusing, very quickly. Watch Jen's video for a clear explanation before you start. 

- LinkedIn Learning Video: [Jen Simmons - Bold and Italics](https://www.linkedin.com/learning/html-essential-training-4/bold-and-italics?u=36102708) 4m 55s

In human language, we often *emphasise* certain words to alter the meaning of a sentence, and we often want to mark certain words as important or different in some way. HTML provides various semantic elements to allow us to mark up textual content with such effects, and in this section, we'll look at a few of the most common ones.

## Emphasis `<em>`

When we want to add emphasis in spoken language, we stress certain words, subtly altering the meaning of what we are saying. Similarly, in written language we tend to stress words by putting them in italics. For example, the following two sentences have different meanings.

I am glad you weren't late.

I am *glad* you weren't late.

The first sentence sounds genuinely relieved that the person wasn't late. In contrast, the second one sounds sarcastic or passive-aggressive, expressing annoyance that the person arrived a bit late (because the emphasis is on the word *glad*).

In HTML we use the `<em>` (emphasis) element to mark up such instances. As well as making the document more interesting to read, these are recognised by screen readers and spoken out in a different tone of voice. Browsers style this as italic by default, but you shouldn't use this tag purely to get italic styling. To do that, you'd use a `<span>` element and some CSS, or perhaps an `<i>` element (see below).

```
<p>I am <em>glad</em> you weren't <em>late</em>.</p>
```

> Gives you a really sarcastic:

<p>I am <em>glad</em> you weren't <em>late</em>.</p>

## Strong importance `<strong>`

To emphasize important words, we tend to stress them in spoken language and bold them in written language. For example:

This liquid is **highly toxic**.

I am counting on you. **Do not** be late!

In HTML we use the `<strong>` (strong importance) element to mark up such instances. As well as making the document more useful, again these are recognized by screen readers and spoken in a different tone of voice. Browsers style this as bold text by default, but you shouldn't use this tag purely to get bold styling. To do that, you'd use a `<span>` element and some CSS, or perhaps a `<b>` element (see below).

```
<p>This liquid is <strong>highly toxic</strong>.</p>

<p>I am counting on you. <strong>Do not</strong> be late!</p>
```
<div style="border: 1px solid rgba(10, 130, 175, 1); padding: 5px; margin-bottom: 5px">
<p>This liquid is <strong>highly toxic</strong>.</p>

<p>I am counting on you. <strong>Do not</strong> be late!</p>
</div>

<p style="margin-top: 5px">You can nest strong and emphasis inside one another if desired:</p>

```
<p>This liquid is <strong>highly toxic</strong> —
if you drink it, <strong>you may <em>die</em></strong>.</p>
```
<div style="border: 1px solid rgba(10, 130, 175, 1); padding: 5px;">
<p>This liquid is <strong>highly toxic</strong> —
if you drink it, <strong>you may <em>die</em></strong>.</p>
</div>

## Italic, bold, underline...


The elements we've discussed so far have clearcut associated semantics. The situation with `<b>`, `<i>`, and `<u>` is somewhat more complicated. They came about so people could write bold, italics, or underlined text in an era when CSS was still supported poorly or not at all. Elements like this, which only affect presentation and not semantics, are known as presentational elements and should no longer be used, because as we've seen before, semantics is so important to accessibility, SEO, etc.

HTML5 redefined `<b>`, `<i>` and `<u>` with new, somewhat confusing, semantic roles.

Here's the best rule of thumb: it's likely appropriate to use `<b>`, `<i>`, or `<u>` to convey a meaning traditionally conveyed with bold, italics, or underline, provided there is no more suitable element. However, it always remains critical to keep an accessibility mindset. The concept of italics isn't very helpful to people using screen readers, or to people using a writing system other than the Latin alphabet.

- `<i>` is used to convey a meaning traditionally conveyed by italic: Foreign words, taxonomic designation, technical terms, a thought...
- `<b>` is used to convey a meaning traditionally conveyed by bold: Key words, product names, lead sentence...
- `<u>` is used to convey a meaning traditionally conveyed by underline: Proper name, misspelling...

<h3 class="warning">Underline means a link</h3>

**Warning**: People strongly associate underlining with hyperlinks. Therefore, on the Web, it's best to underline only links. Use the `<u>` element when it's semantically appropriate, but consider using CSS to change the default underline to something more appropriate on the Web. 

<!-- div class="exercise" -->
## Exercise 3

Adding emphasis and importance to your HTML document.

### Task 1

> Open the `html3` folder.

- Open `exercise-03.html` in your editor.

<img src="media/emphasis-text.png" alt="Screenshot of the plain text for this exercise">

### Task 2

- Edit `exercise-03.html`

- Create the page structure by adding a `<h1>` main heading, `<h2>` sub-headings, and `<p>` paragraphs.

- Save `exercise-03.html`

- View the page in a browser and check it against the illustration below.

### Task 3

- Apply the `<strong>` element to the word **Stop** in the second paragraph.

- Apply the `<em>` element to the words *need you* in the third paragraph.

- Apply the `<b>` element to the words **Slice** and **Insert** in the two instructions.

- Apply the `<i>` element to the journal and article details - (*Lancet 1882*) and (*Journal of Psychology, March, 1883*).

When completed, refresh the page in your browser. Does your page look like this?

<img src="media/emphasis.png" alt="Screenshot of the completed file including strong, em, b and i elements">

### Solution

- This is what your code should look like. 

- For some of you it may be easier to learn by copying our code. 

<img src="media/emphasis-complete.png" alt="Screenshot showing the code">

### Task 4

- Fix any issues and run again to check before you move on.

<!-- end div -->


<p class="submit-work">Exercise 3 completed</p>



<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- MDN: `<em>` - [The Emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)

- MDN: `<strong>` - [The Strong element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)

- MDN: `<i>` - [The Idiomatic Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)

- MDN: `<b>` - [The Bring To Attention element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)

- MDN: `<u>` - [The Unarticulated Annotation (Underline) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u)


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).
