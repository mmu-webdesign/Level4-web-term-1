# HTML table basics

This gets you started with HTML tables, covering the very basics such as rows and cells, headings, making cells span multiple columns and rows, and how to group together all the cells in a column for styling purposes.

<h3 class="warning">New to tables?</h3>

If new to tables, it may help to watch Jen's videos **before** starting to follow the tutorial and exercises. 

- LinkedIn Learning Video: [Jen Simmons -  When to use tables](https://www.linkedin.com/learning/html-essential-training-4/when-to-use-tables?u=36102708) (4m 35s)

- LinkedIn Learning Video: [Jen Simmons -  Building table rows](https://www.linkedin.com/learning/html-essential-training-4/building-table-rows?u=36102708) (3m 11s)

## What is a table ?

A table is a structured set of data made up of rows and columns (**tabular data**). A table allows you to quickly and easily look up values that indicate some kind of connection between different types of data, for example a person and their age, or a day of the week, or the timetable for a local swimming pool.

<img src="https://media.prod.mdn.mozit.cloud/attachments/2017/01/23/14583/5bad217718ecd469850752f2d97b1137/numbers-table.png" alt="A sample table showing names and ages of some people - Chris 38, Dennis 45, Sarah 29, Karen 47">

<img src="https://media.prod.mdn.mozit.cloud/attachments/2017/01/23/14587/3435faac399750fa4ad8877e5644ac6c/swimming-timetable.png" alt="A swimming timetable showing a sample data table">

Tables are very commonly used in human society, and have been for a long time, as evidenced by this US Census document from 1800:

<img src="https://media.prod.mdn.mozit.cloud/attachments/2017/01/23/14585/d2c23cf524bcde948301f7bbf44b1d2b/1800-census.jpg" alt="A very old parchment document; the data is not easily readable, but it clearly shows a data table being used">

It is therefore no wonder that the creators of HTML provided a means by which to structure and present tabular data on the web.

## How does a table work?

The point of a table is that it is rigid. Information is easily interpreted by making visual associations between row and column headers. Look at the table below for example and find a Jovian gas giant with 62 moons. You can find the answer by associating the relevant row and column headers.


Data about the planets of our solar system (Planetary facts taken from [Nasa's Planetary Fact Sheet - Metric](http://nssdc.gsfc.nasa.gov/planetary/factsheet/). 	

<table border="1">
 <caption>Data about the planets of our solar system (Planetary facts taken from <a href="http://nssdc.gsfc.nasa.gov/planetary/factsheet/" rel="noopener">Nasa's Planetary Fact Sheet - Metric</a>.</caption>
 <thead>
  <tr>
   <td colspan="2"></td>
   <th scope="col">Name</th>
   <th scope="col">Mass (10<sup>24</sup>kg)</th>
   <th scope="col">Diameter (km)</th>
   <th scope="col">Density (kg/m<sup>3</sup>)</th>
   <th scope="col">Gravity (m/s<sup>2</sup>)</th>
   <th scope="col">Length of day (hours)</th>
   <th scope="col">Distance from Sun (10<sup>6</sup>km)</th>
   <th scope="col">Mean temperature (°C)</th>
   <th scope="col">Number of moons</th>
   <th scope="col">Notes</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th colspan="2" rowspan="4" scope="rowgroup">Terrestial planets</th>
   <th scope="row">Mercury</th>
   <td>0.330</td>
   <td>4,879</td>
   <td>5427</td>
   <td>3.7</td>
   <td>4222.6</td>
   <td>57.9</td>
   <td>167</td>
   <td>0</td>
   <td>Closest to the Sun</td>
  </tr>
  <tr>
   <th scope="row">Venus</th>
   <td>4.87</td>
   <td>12,104</td>
   <td>5243</td>
   <td>8.9</td>
   <td>2802.0</td>
   <td>108.2</td>
   <td>464</td>
   <td>0</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Earth</th>
   <td>5.97</td>
   <td>12,756</td>
   <td>5514</td>
   <td>9.8</td>
   <td>24.0</td>
   <td>149.6</td>
   <td>15</td>
   <td>1</td>
   <td>Our world</td>
  </tr>
  <tr>
   <th scope="row">Mars</th>
   <td>0.642</td>
   <td>6,792</td>
   <td>3933</td>
   <td>3.7</td>
   <td>24.7</td>
   <td>227.9</td>
   <td>-65</td>
   <td>2</td>
   <td>The red planet</td>
  </tr>
  <tr>
   <th rowspan="4" scope="rowgroup">Jovian planets</th>
   <th rowspan="2" scope="rowgroup">Gas giants</th>
   <th scope="row">Jupiter</th>
   <td>1898</td>
   <td>142,984</td>
   <td>1326</td>
   <td>23.1</td>
   <td>9.9</td>
   <td>778.6</td>
   <td>-110</td>
   <td>67</td>
   <td>The largest planet</td>
  </tr>
  <tr>
   <th scope="row">Saturn</th>
   <td>568</td>
   <td>120,536</td>
   <td>687</td>
   <td>9.0</td>
   <td>10.7</td>
   <td>1433.5</td>
   <td>-140</td>
   <td>62</td>
   <td></td>
  </tr>
  <tr>
   <th rowspan="2" scope="rowgroup">Ice giants</th>
   <th scope="row">Uranus</th>
   <td>86.8</td>
   <td>51,118</td>
   <td>1271</td>
   <td>8.7</td>
   <td>17.2</td>
   <td>2872.5</td>
   <td>-195</td>
   <td>27</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Neptune</th>
   <td>102</td>
   <td>49,528</td>
   <td>1638</td>
   <td>11.0</td>
   <td>16.1</td>
   <td>4495.1</td>
   <td>-200</td>
   <td>14</td>
   <td></td>
  </tr>
  <tr>
   <th colspan="2" scope="rowgroup">Dwarf planets</th>
   <th scope="row">Pluto</th>
   <td>0.0146</td>
   <td>2,370</td>
   <td>2095</td>
   <td>0.7</td>
   <td>153.3</td>
   <td>5906.4</td>
   <td>-225</td>
   <td>5</td>
   <td>Declassified as a planet in 2006, but this <a href="http://www.usatoday.com/story/tech/2014/10/02/pluto-planet-solar-system/16578959/" rel="noopener">remains controversial</a>.</td>
  </tr>
 </tbody>
</table>

When done correctly, even blind people can interpret tabular data in an HTML table — a successful HTML table should enhance the experience of sighted and visually impaired users alike.

## Table styling

You can also have a look at the [live example on GitHub](https://mdn.github.io/learning-area/html/tables/assessment-finished/planets-data.html)! One thing you'll notice is that the table does look a bit more readable there — this is because the table you see above on this page has minimal styling, whereas the GitHub version has more significant CSS applied.

Be under no illusion; for tables to be effective on the web, you need to provide some styling information with CSS, as well as good solid structure with HTML. In this module we are focusing on the HTML part; to find out about the CSS part you should visit MDN's [Styling tables article](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Styling_tables) after you've learnt about CSS.

We won't focus on CSS in this module, but we have provided a minimal CSS stylesheet for you to use that will make your tables more readable than the default you get without any styling. You can find the [stylesheet here](https://github.com/mdn/learning-area/blob/master/html/tables/basic/minimal-table.css), and you can also find an [HTML template](https://github.com/mdn/learning-area/blob/master/html/tables/basic/blank-template.html) that applies the stylesheet — these together will give you a good starting point for experimenting with HTML tables.

<h3 class="warning">When should you NOT use HTML tables?</h3>

**HTML tables should be used for tabular data — this is what they are designed for**. Unfortunately, a lot of people used to use HTML tables to lay out web pages, e.g. one row to contain the header, one row to contain the content columns, one row to contain the footer, etc. You can find more details and an example at [Page Layouts](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML#Page_layouts) in MDN's [Accessibility Learning Module](https://developer.mozilla.org/en-US/docs/Learn/Accessibility). This was commonly used because CSS support across browsers used to be terrible; table layouts are much less common nowadays, but you might still see them in some corners of the web.

In short, using tables for layout rather than CSS layout techniques is a bad idea. The main reasons are as follows:

1. **Layout tables reduce accessibility for visually impaired users**: [Screenreaders](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/Accessibility#Screenreaders), used by blind people, interpret the tags that exist in an HTML page and read out the contents to the user. Because tables are not the right tool for layout, and the markup is more complex than with CSS layout techniques, the screenreaders' output will be confusing to their users.

1. **Tables produce tag soup**: As mentioned above, table layouts generally involve more complex markup structures than proper layout techniques. This can result in the code being harder to write, maintain, and debug.

1. **Tables are not automatically responsive**: When you use proper layout containers (such as `<header>`, `<section>`, `<article>`, or `<div>`), their width defaults to 100% of their parent element. Tables on the other hand are sized according to their content by default, so extra measures are needed to get table layout styling to effectively work across a variety of devices.

## Exercise: Creating your first table

We've talked table theory enough, so, let's dive into a practical example and build up a simple table.

1. First of all, make a local copy of blank-template.html and minimal-table.css in a new directory on your local machine.

1. The content of every table is enclosed by these two tags : `<table></table>`. Add these inside the body of your HTML.

1. The smallest container inside a table is a table cell, which is created by a `<td>` element (**'td' stands for 'table data'**). Add the following inside your table tags:

```
<td>Hi, I'm your first cell.</td>
```

4. If we want a row of four cells, we need to copy these tags three times. Update the contents of your table to look like so:

```
<td>Hi, I'm your first cell.</td>
<td>I'm your second cell.</td>
<td>I'm your third cell.</td>
<td>I'm your fourth cell.</td>
```

As you will see, the cells are not placed underneath each other, rather they are automatically aligned with each other on the same row. Each `<td>` element creates a single cell and together they make up the first row. Every cell we add makes the row grow longer.

To stop this row from growing and start placing subsequent cells on a second row, we need to use the `<tr>` element (**'tr' stands for 'table row'**). Let's investigate this now.

1. Place the four cells you've already created inside `<tr>` tags, like so:

```
<tr>
    <td>Hi, I'm your first cell.</td>
    <td>I'm your second cell.</td>
    <td>I'm your third cell.</td>
    <td>I'm your fourth cell.</td>
</tr>
```

2. Now you've made one row, have a go at making one or two more — each row needs to be wrapped in an additional `<tr>` element, with each cell contained in a `<td>`.

This should result in a table that looks something like the following:

<table border="1">
 <tbody>
  <tr>
   <td>Hi, I'm your first cell.</td>
   <td>I'm your second cell.</td>
   <td>I'm your third cell.</td>
   <td>I'm your fourth cell.</td>
  </tr>
  <tr>
   <td>Second row, first cell.</td>
   <td>Cell 2.</td>
   <td>Cell 3.</td>
   <td>Cell 4.</td>
  </tr>
 </tbody>
</table>

> Note: You can also find this on GitHub as [simple-table.html](https://github.com/mdn/learning-area/blob/master/html/tables/basic/simple-table.html) ([see it live also](http://mdn.github.io/learning-area/html/tables/basic/simple-table.html)).

## Adding headers with `<th>` elements

Now let's turn our attention to table headers — special cells that go at the start of a row or column and define the type of data that row or column contains (as an example, see the "Person" and "Age" cells in the first example shown in this article). To illustrate why they are useful, have a look at the following table example. First the source code:

```
<table>
  <tr>
    <td>&nbsp;</td>
    <td>Knocky</td>
    <td>Flor</td>
    <td>Ella</td>
    <td>Juan</td>
  </tr>
  <tr>
    <td>Breed</td>
    <td>Jack Russell</td>
    <td>Poodle</td>
    <td>Streetdog</td>
    <td>Cocker Spaniel</td>
  </tr>
  <tr>
    <td>Age</td>
    <td>16</td>
    <td>9</td>
    <td>10</td>
    <td>5</td>
  </tr>
  <tr>
    <td>Owner</td>
    <td>Mother-in-law</td>
    <td>Me</td>
    <td>Me</td>
    <td>Sister-in-law</td>
  </tr>
  <tr>
    <td>Eating Habits</td>
    <td>Eats everyone's leftovers</td>
    <td>Nibbles at food</td>
    <td>Hearty eater</td>
    <td>Will eat till he explodes</td>
  </tr>
</table>
```
Now the actual rendered table:

<table border="1">
 <tbody>
  <tr>
   <td></td>
   <td>Knocky</td>
   <td>Flor</td>
   <td>Ella</td>
   <td>Juan</td>
  </tr>
  <tr>
   <td>Breed</td>
   <td>Jack Russell</td>
   <td>Poodle</td>
   <td>Streetdog</td>
   <td>Cocker Spaniel</td>
  </tr>
  <tr>
   <td>Age</td>
   <td>16</td>
   <td>9</td>
   <td>10</td>
   <td>5</td>
  </tr>
  <tr>
   <td>Owner</td>
   <td>Mother-in-law</td>
   <td>Me</td>
   <td>Me</td>
   <td>Sister-in-law</td>
  </tr>
  <tr>
   <td>Eating Habits</td>
   <td>Eats everyone's leftovers</td>
   <td>Nibbles at food</td>
   <td>Hearty eater</td>
   <td>Will eat till he explodes</td>
  </tr>
 </tbody>
</table>

The problem here is that, while you can kind of make out what's going on, it is not as easy to cross reference data as it could be. If the column and row headings stood out in some way, it would be much better.

## Exercise: table headers

Let's have a go at improving this table.

1. First, make a local copy of MDN's [dogs-table.html](https://github.com/mdn/learning-area/blob/master/html/tables/basic/dogs-table.html) and [minimal-table.css](https://github.com/mdn/learning-area/blob/master/html/tables/basic/minimal-table.css) files in a new directory on your local machine. The HTML contains the same Dogs example as you saw above.

1. To recognize the table headers as headers, both visually and semantically, you can use the `<th>` element ('th' stands for 'table header'). This works in exactly the same way as a `<td>`, except that it denotes a header, not a normal cell. Go into your HTML, and change all the `<td>` elements surrounding the table headers into `<th>` elements.

1. Save your HTML and load it in a browser, and you should see that the headers now look like headers.

> Note: You can find our finished example at [dogs-table-fixed.html](https://github.com/mdn/learning-area/blob/master/html/tables/basic/dogs-table-fixed.html) on GitHub ([see it live also](http://mdn.github.io/learning-area/html/tables/basic/dogs-table-fixed.html)).


### Why are headers useful?

We have already partially answered this question — it is easier to find the data you are looking for when the headers clearly stand out, and the design just generally looks better.

> Note: Table headings come with some default styling — they are bold and centered even if you don't add your own styling to the table, to help them stand out.

Tables headers also have an added benefit — along with the scope attribute (which we'll learn about in the next article), they allow you to make tables more accessible by associating each header with all the data in the same row or column. Screenreaders are then able to read out a whole row or column of data at once, which is pretty useful.

## Allowing cells to span multiple rows and columns

Sometimes we want cells to span multiple rows or columns. Take the following simple example, which shows the names of common animals. In some cases, we want to show the names of the males and females next to the animal name. Sometimes we don't, and in such cases we just want the animal name to span the whole table.

The initial markup looks like this:

```
<table>
  <tr>
    <th>Animals</th>
  </tr>
  <tr>
    <th>Hippopotamus</th>
  </tr>
  <tr>
    <th>Horse</th>
    <td>Mare</td>
  </tr>
  <tr>
    <td>Stallion</td>
  </tr>
  <tr>
    <th>Crocodile</th>
  </tr>
  <tr>
    <th>Chicken</th>
    <td>Hen</td>
  </tr>
  <tr>
    <td>Rooster</td>
  </tr>
</table>
```
But the output doesn't give us quite what we want:

<table border="1">
 <tbody>
  <tr>
   <th>Animals</th>
  </tr>
  <tr>
   <th>Hippopotamus</th>
  </tr>
  <tr>
   <th>Horse</th>
   <td>Mare</td>
  </tr>
  <tr>
   <td>Stallion</td>
  </tr>
  <tr>
   <th>Crocodile</th>
  </tr>
  <tr>
   <th>Chicken</th>
   <td>Hen</td>
  </tr>
  <tr>
   <td>Rooster</td>
  </tr>
 </tbody>
</table>

We need a way to get "Animals", "Hippopotamus", and "Crocodile" to span across two columns, and "Horse" and "Chicken" to span downwards over two rows. Fortunately, table headers and cells have the `colspan` and `rowspan` attributes, which allow us to do just those things. Both accept a unitless number value, which equals the number of rows or columns you want spanned. For example, `colspan="2"` makes a cell span two columns.

Let's use `colspan` and `rowspan` to improve this table.

1. First, make a local copy of our [animals-table.html](https://github.com/mdn/learning-area/blob/master/html/tables/basic/animals-table.html) and [minimal-table.css](https://github.com/mdn/learning-area/blob/master/html/tables/basic/minimal-table.css) files in a new directory on your local machine. The HTML contains the same animals example as you saw above.

1. Next, use `colspan` to make "Animals", "Hippopotamus", and "Crocodile" span across two columns.

1. Finally, use `rowspan` to make "Horse" and "Chicken" span across two rows.
Save and open your code in a browser to see the improvement.

> Note: You can find our finished example at [animals-table-fixed.html](https://github.com/mdn/learning-area/blob/master/html/tables/basic/animals-table-fixed.html) on GitHub ([see it live also](http://mdn.github.io/learning-area/html/tables/basic/animals-table-fixed.html)).

<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- MDN: `<table>` - [The Table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)

- MDN: `<tr>` - [The Table Row element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr)

- MDN: `<td>` - [The Table Data Cell element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td)

- MDN: `<th>` - [The Table Header element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th)

