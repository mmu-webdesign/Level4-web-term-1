# Borders and padding

## Borders

The border is drawn between the margin and the padding of a box. If you are using the standard box model, the size of the border is added to the `width` and `height` of the box. If you are using the alternative box model then the size of the border makes the content box smaller as it takes up some of that available `width` and `height`.

For styling borders, there are a large number of properties — there are four borders, and each border has a style, width and color that we might want to manipulate.

You can set the width, style, or color of all four borders at once using the [border property](https://developer.mozilla.org/en-US/docs/Web/CSS/border).

To set the properties of each side individually, you can use:

- [border-top](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top)
- [border-right](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right)
- [border-bottom](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom)
- [border-left](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left)


To set the width, style, or color of all sides, use the following:

The `border-width` shorthand CSS property sets the width of an element's border. Border width can be applied with keywords and length values:

```
/* Keyword values */
border-width: thin;
border-width: medium;
border-width: thick;

/* <length> values */
border-width: 4px;
border-width: 1.2rem;
```

- MDN's [border-width](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width) reference.

The `border-style` shorthand CSS property sets the line style for all four sides of an element's border. Border style is applied with keywords. These can look pretty awful so apply/use with care.

```
/* Keyword values */
border-style: none;
border-style: hidden;
border-style: dotted;
border-style: dashed;
border-style: solid;
border-style: double;
border-style: groove;
border-style: ridge;
border-style: inset;
border-style: outset;
```

- MDN's [border-style](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style) reference.

The `border-color` shorthand CSS property sets the color of an element's border. Colour can be applied in the usual ways including colour name, hex, rgb, rgba etc.

```
border-color: red;

border-color: #32a1ce;

border-color: rgba(170, 50, 220, .6);

```

- MDN's [border-color](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) reference.

To set the width, style, or color of a single side, you can use one of the most granular longhand properties:

<ul>
 <li><a href="/en-US/docs/Web/CSS/border-top-width"><code>border-top-width</code></a> - sets the width of the top border of an element.</li>
 <li><a href="/en-US/docs/Web/CSS/border-top-style"><code>border-top-style</code></a> - sets the line style of an element's top border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-top-color"><code>border-top-color</code></a> - sets the color of an element's top border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-right-width"><code>border-right-width</code></a> - sets the width of the right border of an element.</li>
 <li><a href="/en-US/docs/Web/CSS/border-right-style"><code>border-right-style</code></a> - sets the line style of an element's right border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-right-color"><code>border-right-color</code></a> - sets the color of an element's right border. It can also be set with the shorthand CSS properties border-color or border-right.</li>
 <li><a href="/en-US/docs/Web/CSS/border-bottom-width"><code>border-bottom-width</code></a> - sets the width of the bottom border of an element.</li>
 <li><a href="/en-US/docs/Web/CSS/border-bottom-style"><code>border-bottom-style</code></a> - sets the line style of an element's bottom border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-bottom-color"><code>border-bottom-color</code></a> - sets the color of an element's bottom border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-left-width"><code>border-left-width</code></a> - sets the width of the left border of an element.</li>
 <li><a href="/en-US/docs/Web/CSS/border-left-style"><code>border-left-style</code></a> - sets the line style of an element's left border.</li>
 <li><a href="/en-US/docs/Web/CSS/border-left-color"><code>border-left-color</code></a> - sets the color of an element's left border.</li>
</ul>

### Shorthand

As with margins, you can use shorthand (clockwise) to apply border styles.

-   When one value is specified, it applies the same width to all four sides.
```
/* <length> values */
border-width: 1.2rem;
border-style: dotted;
border-color: red;
```
- When two values are specified, the first width applies to the top and bottom, the second to the left and right.

```
/* vertical | horizontal */
border-width: 2px 1.5em;
border-style: dotted solid;
border-color: red #f015ca;
```
- When three values are specified, the first width applies to the top, the second to the left and right, the third to the bottom.
```
/* top | horizontal | bottom */
border-width: 1px 2em 1.5cm;
border-style: hidden double dashed;
border-color: red rgb(240,30,50,.7) green;
```
- When four values are specified, the widths apply to the top, right, bottom, and left in that order (clockwise).
```
/* top | right | bottom | left */
border-width: 1px 2em 0 4rem;
border-style: none solid dotted dashed;
border-color: red yellow green blue; 
```

With borders, the width, color, and style can be simplified into one declaration. For example, the following CSS ...

```
border-width: 1px;
border-style: solid;
border-color: #000;
```

... can be simplified as:

```
border: 1px solid #000;
```


## Padding

The padding sits between the border and the content area. Unlike margins you cannot have negative amounts of padding, so the value must be 0 or a positive value. Any background applied to your element will display behind the padding, and it is typically used to push the content away from the border.

YOu will note that Derren prefers to use (when possible) `padding` rather than `margin` to create space between elements. 

We can control the padding on each side of an element individually using the padding property, or each side individually using the equivalent longhand properties:

    padding-top
    padding-right
    padding-bottom
    padding-left


<!-- div class="exercise" -->
## Exercise 11

<!-- end div -->

<p class="submit-work">Exercise 11 completed</p>



<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

MD's [Shorthand properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties) reference page looks at various ways of applying shorthand to margins, borders, padding, and fonts.


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).




