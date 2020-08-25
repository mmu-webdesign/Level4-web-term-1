# More links

## Document fragments

It is possible to link to a specific part of an HTML document (known as a document fragment), rather than just to the top of the document. To do this you first have to assign an id attribute to the element you want to link to. It normally makes sense to link to a specific heading, so this would look something like the following:

```
<h2 id="Mailing_address">Mailing address</h2>
```

Then to link to that specific id, you'd include it at the end of the URL, preceded by a hash/pound symbol, for example:

```
<p>Want to write us a letter? Use our <a href="contacts.html#Mailing_address">mailing address</a>.</p>
```

You can even use the document fragment reference on its own to link to another part of the same document:

```
<p>The <a href="#Mailing_address">company mailing address</a> can be found at the bottom of this page.</p>
```

<!-- div class="exercise" -->
## Exercise One

> Internal links - creating links within (to a specific part of) a document.

### Task 1

- Open [Repl.it - Internal Links](https://repl.it/@webdesignmmu/html8)

What you have is a document with a *table of contents* (menu) at the top, followed by three sections of text. In this exercise you are going to link each menu item to the relevant section. Allowing the reader to *jump* to the relevant section.

### Task 2

- The menu is well spaced out so you can identify the section names, e.g. Section One. 

```
<ul>
  <li>
    Section One
  </li>
  <li>
    Section Two
  </li>
  <li>
    Section Three
  </li>
</ul>
```

- Wrap each section title with a `<a>` element as below:

```
  <li>
    <a>Section One</a>
  </li>
```
- Do this for all three sections listed.

### Task 3

- Add the `href=""` attribute to each of the three opening `<a>` tags.

```
  <li>
    <a href="">Section One</a>
  </li>
  
  ```
- If you Run the page in the browser you will now see the menu items look like links (blue/purple underlined text). 
- Clicking on them does nothing - as we haven't defined the link location in the `href=""` attribute.

### Task 4

- Adding the link location - but this time it's not an URL or file path. We are going to link to a named element on the page using an `ID` or `#` attribute.

- As we are linking to each section we are going to use the name of the section, for example `#one` for Section One.

- Do this for each link starting with:

```
<a href="#one">Section One</a>
```

- Obviously `#two` and `#three` for the other two.

Nothing changes on our page as the destinations have yet to be defined.

### Task 5

- For this to work we need to add `IDs` (names) to the link targets - where we want the menu to take us to.

- We do this by adding the ID attribute `id="one"`, to our Section One heading. As follows.

```
<h2 id="one">Section One</h2>
```
- Run the page again.

- If you've got it right, when you click to Section One link in the menu the page will *jump down* to Section One.

- If that has worked, do the same for sections two and three, obviously using `id="two"` and `id="three"`.

- Run your page and check all three links.

<figure>
<video controls>
  <source src="media/internal-links.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="media/internal-links.mp4">link to the video</a> instead.</p>
</video>
  <figcaption>The video illustrates the menu links working, creating links to the various sections of the document.</figcaption>
</figure>

<!-- end div -->

### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).