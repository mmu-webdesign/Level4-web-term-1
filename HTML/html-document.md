# Anatomy of an HTML document

Individual HTML elements aren't very useful on their own. Next, let's examine how individual elements combine to form an entire HTML page:

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```

Here we have:

1. `<!DOCTYPE html>`: The doctype. When HTML was young (1991-1992), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML. Doctypes used to look something like this:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```
More recently, the doctype is a historical artifact that needs to be included for everything else to work right. `<!DOCTYPE html>` is the shortest string of characters that counts as a valid doctype. **That is all you need to know!**

2. `<html></html>`: The `<html>` element. This element wraps all the content on the page. It is sometimes known as the root element.

1. `<head></head>`: The `<head>` element. This element acts as a container for everything you want to include on the HTML page, that isn't the content the page will show to viewers. This includes keywords and a page description that would appear in search results, CSS to style content, character set declarations, and more. 

1. `<meta charset="utf-8">`: This element specifies the character set for your document to UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.
1. `<title></title>`: The `<title>` element. This sets the title of the page, which is the title that appears in the browser tab the page is loaded in. The page title is also used to describe the page when it is bookmarked.
1. `<body></body>`: The `<body>` element. This contains all the content that displays on the page, including text, images, videos, games, playable audio tracks, or whatever else.

<div class="deep">
## Deeper Learning
To get a better understanding of this topic use the following resources.

- LinkedIn Learning Video: [Jen Simmons -  The html page](https://www.linkedin.com/learning/html-essential-training-4/the-html-page?u=36102708) (5m 1s)

- MDN: `<!DOCTYPE html>` - [Doctype](https://developer.mozilla.org/en-US/docs/Glossary/Doctype)

- MDN: `<html>` - [The HTML Document / Root element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html)

- MDN: `<body>` - [The Document Body element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)

</div>

### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).