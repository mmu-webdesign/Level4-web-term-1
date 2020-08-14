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

## Absolute versus relative URLs

Two terms you'll come across on the Web are **absolute URL** and **relative URL**:

**Absolute URL**: Points to a location defined by its absolute location on the web, including protocol and domain name. So for example, if an `index.html` page is uploaded to a directory called `projects` that sits inside the root of a web server, and the web site's domain is `http://www.example.com`, the page would be available at `http://www.example.com/projects/index.html` (or even just `http://www.example.com/projects/`, as most web servers just look for a landing page such as `index.html` to load if it is not specified in the URL.)

An absolute URL will always point to the same location, no matter where it is used.

**relative URL**: Points to a location that is relative to the file you are linking from, more like what we looked at in the previous section. For example, if we wanted to link from our example file at `http://www.example.com/projects/index.html` to a PDF file in the same directory, the URL would just be the filename — e.g. `project-brief.pdf` — no extra information needed. If the PDF was available in a subdirectory inside projects called `pdfs`, the relative link would be `pdfs/project-brief.pdf` (the equivalent absolute URL would be `http://www.example.com/projects/pdfs/project-brief.pdf`.)

A relative URL will point to different places depending on the actual location of the file you refer from — for example if we moved our `index.html` file out of the projects directory and into the root of the web site (the top level, not in any directories), the `pdfs/project-brief.pdf` relative URL link inside it would now point to a file located at `http://www.example.com/pdfs/project-brief.pdf`, not a file located at `http://www.example.com/projects/pdfs/project-brief.pdf`.

Of course, the location of the `project-brief.pdf` file and pdfs folder won't suddenly change because you moved the index.html file — this would make your link point to the wrong place, so it wouldn't work if clicked on. You need to be careful!

<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons - Navigation](https://www.linkedin.com/learning/html-essential-training-4/navigation?u=36102708) (3m 19s)

### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).