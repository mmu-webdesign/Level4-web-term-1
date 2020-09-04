# Color

There are many ways to specify color in CSS, some of which are more recently implemented than others. The same color values can be used everywhere in CSS, whether you are specifying text color, background color, or whatever else.

The standard color system available in modern computers is 24 bit, which allows the display of about 16.7 million distinct colors via a combination of different red, green and blue channels with 256 different values per channel (256 x 256 x 256 = 16,777,216.) Let's have a look at some of the ways in which we can specify colors in CSS.

> Note: In this tutorial we will look at the common methods of specifying color that have good browser support; there are others but they don't have as good support and are less common.

## Color keywords

So far you will see the color keywords used, as they are a simple and understandable way of specifying color. There are a number of these keywords, some of which have fairly entertaining names! 

You can see a full list on the page for the [color value](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).

Color keywords are case-insensitive identifiers that represent a specific color, such as `red`, `blue`, `black`, or `lightseagreen`. Although the names more or less describes their respective colors, they are essentially artificial, without a strict rationale behind the names used.

This site [neilorangepeel.com](https://colours.neilorangepeel.com/) is a great resource to see all of the colour names. It also provides their `hex` and `rgb` values (to follow).

## Hexadecimal RGB values

The next type of color value you are likely to encounter is **hexadecimal codes**. Each `hex` value consists of a hash/pound symbol (`#`) followed by six hexadecimal numbers, each of which can take one of 16 values between `0` and `f` (which represents `15`) — so `0123456789abcdef`. Each pair of values represents one of the channels — red, green and blue — and allows us to specify any of the 256 available values for each (16 x 16 = 256.)

These values are a bit more complex and less easy to understand, but they are a lot more versatile than keywords — you can use hex values to represent any color you want to use in your color scheme.

<!-- div class="exercise" -->
## Exercise One

> Using `hex` values.

### Task 1

- Open the exercise files in another browser window - [Repl.it - colour](https://repl.it/@webdesignmmu/css05)

### Task 2

- Add the following CSS to `style.css`:

```
body {
  color:#5a5a5a;
  background-color: #f9f9f9;
}
```
- Applying styles to the `body`, applies the styles to everything in the browser window.

- Run `index.html` in the browser.

- `color:#5a5a5a;` gives us grey text (headings and paragraphs).

- `background-color: #f9f9f9;` gives us an off-white background to the whole page.

### Task 2

- Add the following CSS to `style.css`:

```
a:link {
    color: #333;
}

a:visited {
    color: #000;
}

a:hover {
    text-decoration: none;
    background-color: #fcf9d1;
}
```
- Run in the browser to test the effect.

- Once again we are styling the various link states with these pseudo selectors.

- `background-color: #fcf9d1;` is added to our hover effect.

### Task 3

- Adjust `body` colours to create your own colour scheme.

```
body {
  color:#;
  background-color: #;
}
```

- Add hex codes using the [website coolors.co](https://coolors.co/) to discover a colour scheme and the hex codes.

- Do this, keeping in mind good colour contrast. The text must be legible - **Much more on this later**.

<p style="color:#30323D; background-color:#4D5061; padding: 5px;">This is not good. This is not good. This is not good.</p>

- Selecting the *right* colours or *good* colours is hard but ive it a try. 

- Beware you will note that Repl.it likes to add colours using RGB - that's next.

<!-- end div -->




<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Colour property](https://www.linkedin.com/learning/css-essential-training-3/the-color-and-property-values?u=36102708)



### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).