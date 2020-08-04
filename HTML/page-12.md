# Code, Entity Characters and Superscript/subscript

## Representing computer code

There are a number of elements available for marking up computer code using HTML:

- `<code>`: For marking up generic pieces of computer code.

- `<pre>`: For retaining whitespace (generally code blocks) 
— if you use indentation or excess whitespace inside your text, browsers will ignore it and you will not see it on your rendered page. If you wrap the text in `<pre></pre>` tags however, your whitespace will be rendered identically to how you see it in your text editor.

There are others including `<var>` [Variable element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var) for specifically marking up variable names. `<kbd>` the [Keyboard Input element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd) for marking up keyboard (and other types of) input entered into the computer and `<samp>` the [Sample Output element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp) for marking up the output of a computer program.

These all have limited use. Perhaps the most common is the use of `<code>`, for example: 

```
<code>var para = document.querySelector('p');</code>

```
The above code will look like so:

<div class="output">
<code>var para = document.querySelector('p');</code>
</div>

It's handy to know that if you want to put code on a page you can also use special characters to create the angled brackets. See the next section.

And `<pre>` can be handy for showing text indented as intended:

<div class="output">

<pre>
To       be

  
  or  not                to be

                                   is the question.
</pre>

</div>


## Entity references: Including special characters in HTML

In HTML, the characters `<`, `>`,`"`,`'` and & are special characters. They are parts of the HTML syntax itself. So how do you include one of these special characters in your text? For example, if you want to use an ampersand or less-than sign, and not have it interpreted as code.

You do this with character references. These are special codes that represent characters, to be used in these exact circumstances. Each character reference starts with an ampersand (&), and ends with a semicolon (;).

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Literal character</th>
   <th scope="col">Character reference equivalent</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>&lt;</td>
   <td>&amp;lt;</td>
  </tr>
  <tr>
   <td>&gt;</td>
   <td>&amp;gt;</td>
  </tr>
  <tr>
   <td>"</td>
   <td>&amp;quot;</td>
  </tr>
  <tr>
   <td>'</td>
   <td>&amp;apos;</td>
  </tr>
  <tr>
   <td>&amp;</td>
   <td>&amp;amp;</td>
  </tr>
 </tbody>
</table>

The character reference equivalent could be easily remembered because the text it uses can be seen as less than for '`&lt;`' , quotation for '`&quot;`' and similarly for others. To find more about entity reference, see [List of XML and HTML character entity references](http://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references) (Wikipedia).

In the example below, there are two paragraphs:

```
<p>In HTML, you define a paragraph using the <p> element.</p>

<p>In HTML, you define a paragraph using the &lt;p&gt; element.</p>

```
In the live output below, you can see that the first paragraph has gone wrong. The browser interprets the second instance of `<p>` as starting a new paragraph. The second paragraph looks fine because it has angle brackets with character references.

<div class="output">

<p>In HTML, you define a paragraph using the <p> element.</p>

<p>In HTML, you define a paragraph using the &lt;p&gt; element.</p>

</div>

> Note: You don't need to use entity references for any other symbols, as modern browsers will handle the actual symbols just fine as long, as your HTML's character encoding is set to UTF-8.

## Superscript and subscript

You will occasionally need to use superscript and subscript when marking up items like dates, chemical formulae, and mathematical equations so they have the correct meaning. The `<sup>` and `<sub>` elements handle this job. For example:

```
<p>My birthday is on the 25<sup>th</sup> of May 2001.</p>

<p>Caffeine's chemical formula is C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.</p>

<p>If x<sup>2</sup> is 9, x must equal 3 or -3.</p>
```

The output of this code looks like so:

<div class="output">
<p>My birthday is on the 25<sup>th</sup> of May 2001.</p>

<p>Caffeine's chemical formula is C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.</p>

<p>If x<sup>2</sup> is 9, x must equal 3 or -3.</p>
</div>

## Deeper Learning
To get a better understanding of this topic use the following resources.

> LinkedIn Learning Video: [Jen Simmons - Code, pre and br](https://www.linkedin.com/learning/html-essential-training-4/code-pre-and-br?u=36102708) 4m 42s

> LinkedIn Learning Video: [Jen Simmons - Special Characters](https://www.linkedin.com/learning/html-essential-training-4/weird-characters?u=36102708) 3m 21s

> LinkedIn Learning Video: [Jen Simmons - Superscript and subscript](https://www.linkedin.com/learning/html-essential-training-4/superscripts-subscripts-and-small-text?u=36102708) 4m 48s - we will be looking at image formats in greater detail later, but this provides a good introduction.

> MDN: `<code>` - [The Inline Code element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code)

> MDN: `<pre>` - [The Preformatted Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre)

> MDN: `<sub>` - [The Subscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub)

> MDN: `<sup>` - [The Superscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup)

> MDN: `<code>` - [The Inline Code element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code)
