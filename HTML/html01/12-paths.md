# A quick primer on URLs and paths

To fully understand link targets, you need to understand URLs and file paths. This chapter gives you the information you need to achieve this.

A URL, or Uniform Resource Locator is simply a string of text that defines where something is located on the Web. For example, MMUs homepage is located at https://www.mmu.ac.uk.

URLs use paths to find files. Paths specify where in the filesystem the file you are interested in is located. Let's look at a simple example of a directory structure (see the live version - <a href="https://github.com/mdn/learning-area/tree/master/html/introduction-to-html/creating-hyperlinks">creating-hyperlinks directory</a>.)

<img src="media/simple-directory.png" alt="File and folder illustration">

## A simple directory structure.

> Note - The term `directory` refers to the way a structured list of document `files` and `folders` is stored on the computer. [Wikipedia](https://en.wikipedia.org/wiki/Directory_(computing))

In the example above the parent directory is called `creating-hyperlinks` and contains two files called `index.html` and `contacts.html`, and two directories called `projects` and `pdfs`, which contain an `index.html` and a `project-brief.pdf` file, respectively

The root of this directory (folder) structure is called `creating-hyperlinks`. When working locally with a web site, you will have one directory that the whole site goes inside. Inside the root, we have an `index.html` file and a `contacts.html`. In a real website, `index.html` would be our home page or landing page (a web page that serves as the entry point for a website or a particular section of a website.)

There are also two directories (folder) inside our root — `pdfs` and `projects`. These each have a single file inside them — a PDF (`project-brief.pdf`) and an ```index.html``` file, respectively. Note that you can quite happily have two ``index.html`` files in one project, as long as they are in different locations in the filesystem. Many web sites do. The second `index.html` would perhaps be the main landing page for project-related information.

- **Same directory**: If you wanted to include a hyperlink inside `index.html` (the top level `index.html`) pointing to `contacts.html`, you would just need to specify the filename of the file you want to link to, as it is in the same directory as the current file. So the URL you would use is `contacts.html`:

```
<p>Want to contact a specific staff member?
Find details on our <a href="contacts.html">contacts page</a>.</p>
```

- **Moving down into subdirectories**: If you wanted to include a hyperlink inside `index.html` (the top level `index.html`) pointing to `projects/index.html`, you would need to go down into the projects directory before indicating the file you want to link to. This is done by specifying the directory's name, then a forward slash, then the name of the file. so the URL you would use is `projects/index.html`:

```
<p>Visit my <a href="projects/index.html">project homepage</a>.</p>
```

- Moving back up into parent directories: If you wanted to include a hyperlink inside `projects/index.html` pointing to `pdfs/project-brief.pdf`, you'd have to go up a directory level, then back down into the pdf directory. "Go up a directory" is indicated using two dots — .. — so the URL you would use is `../pdfs/project-brief.pdf`:

```
<p>A link to my <a href="../pdfs/project-brief.pdf">project brief</a>.</p>
```

> Note: You can combine multiple instances of these features into complex URLs, if needed, e.g. `../../../complex/path/to/my/file.html`.


## Task One - Paths




<h2 class="deep">Deeper Learning</h2>

To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons - URL paths](https://www.linkedin.com/learning/html-essential-training-4/url-paths?u=36102708) (4m 45s)


### &copy; Credit given

Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).