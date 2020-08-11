# Lists

Now let's turn our attention to lists. Lists are everywhere in life — from your shopping list to the list of directions you subconsciously follow to get to your house every day, to the lists of instructions you are following in these tutorials! Lists are everywhere on the Web too, and we've got three different types to worry about.

## Unordered

Unordered lists are used to mark up lists of items for which the order of the items doesn't matter — let's take a shopping list as an example.

```
milk
eggs
bread
hummus
```

Every unordered list starts off with a `<ul>` element — this wraps around all the list items:

```
<ul>
milk
eggs
bread
hummus
</ul>
```

The last step is to wrap each list item in a `<li>` (list item) element:

```
<ul>
  <li>milk</li>
  <li>eggs</li>
  <li>bread</li>
  <li>hummus</li>
</ul>
```

## Ordered

Ordered lists are lists in which the order of the items does matter — let's take a set of directions as an example:

```
Drive to the end of the road
Turn right
Go straight across the first two roundabouts
Turn left at the third roundabout
The school is on your right, 300 meters up the road
```

The markup structure is the same as for unordered lists, except that you have to wrap the list items in an `<ol>` element, rather than `<ul>`:

```
<ol>
  <li>Drive to the end of the road</li>
  <li>Turn right</li>
  <li>Go straight across the first two roundabouts</li>
  <li>Turn left at the third roundabout</li>
  <li>The school is on your right, 300 meters up the road</li>
</ol>
```

## Description lists

The third type of list you'll occasionally come across — description lists. The purpose of these lists is to mark up a set of items and their associated descriptions, such as terms and definitions, or questions and answers. Let's look at an example of a set of terms and definitions:

```
soliloquy

In drama, where a character speaks to themselves, representing their inner thoughts or feelings and in the process relaying them to the audience (but not to other characters.)

monologue

In drama, where a character speaks their thoughts out loud to share them with the audience and any other characters present.

aside

In drama, where a character shares a comment only with the audience for humorous or dramatic effect. This is usually a feeling, thought or piece of additional background information
```

Description lists use a different wrapper than the other list types — `<dl>`; in addition each term is wrapped in a `<dt>` (description term) element, and each description is wrapped in a `<dd> `(description definition) element. 

> Let's finish marking up our example:

```
<dl>
  <dt>soliloquy</dt>

    <dd>In drama, where a character speaks to themselves, representing their inner thoughts or feelings and in the process relaying them to the audience (but not to other characters.)</dd>
  
  <dt>monologue</dt>

    <dd>In drama, where a character speaks their thoughts out loud to share them with the audience and any other characters present.</dd>

  <dt>aside</dt>

    <dd>In drama, where a character shares a comment only with the audience for humorous or dramatic effect. This is usually a feeling, thought, or piece of additional background information.</dd>
</dl>
```

The browser default styles will display description lists with the descriptions indented somewhat from the terms. 

> It will look like this:

<dl>
  <dt>soliloquy</dt>

  <dd>In drama, where a character speaks to themselves, representing their inner thoughts or feelings and in the process relaying them to the audience (but not to other characters.)</dd>

  <dt>monologue</dt>

  <dd>In drama, where a character speaks their thoughts out loud to share them with the audience and any other characters present.</dd>

  <dt>aside</dt>

  <dd>In drama, where a character shares a comment only with the audience for humorous or dramatic effect. This is usually a feeling, thought, or piece of additional background information.</dd>

</dl>

> Note that it is permitted to have a single term with multiple descriptions, for example:

```
<dl>
  <dt>aside</dt>

    <dd>In drama, where a character shares a comment only with the audience for humorous or dramatic effect. This is usually a feeling, thought, or piece of additional background information.</dd>

    <dd>In writing, a section of content that is related to the current topic, but doesn't fit directly into the main flow of content so is presented nearby (often in a box off to the side.)</dd>
</dl>
```

> Which will display in the browser like this:

<dl>
  <dt>aside</dt>
  <dd>In drama, where a character shares a comment only with the audience for humorous or dramatic effect. This is usually a feeling, thought, or piece of additional background information.</dd>
  <dd>In writing, a section of content that is related to the current topic, but doesn't fit directly into the main flow of content so is presented nearby (often in a box off to the side.)</dd>
</dl>

<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons - Lists](https://www.linkedin.com/learning/html-essential-training-4/lists?autoplay=true&resume=false&u=36102708) (5m 6s)

- MDN: `<ul>` - [The Unordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)

- MDN: `<li>` - [The List Item element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)

- MDN: `<ol>` - [The Ordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)

- MDN: `<dl>` - [The Bring To Attention element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)

- MDN: `<dt>` - [The Description Term element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt)


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).


