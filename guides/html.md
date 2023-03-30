# learn html

## Introduction

HTML is a very simple coding language and it's very easy to learn. Seriously, I'm not joking! All you really need to know to write HTML is a few tags! HTML is just a language that tells web browsers like Google Chrome and Firefox how to format text on a page, the majority of HTML code is actually usually just text contained within tags. Tags are what opens and closes an HTML element.

For example, if I wanted to start a new paragraph I would communicate that to the browser by writing `<p>` and to end that paragraph I would write `</p>`

Everything contained in between `<p>` and `</p>` is considered a "paragraph element."  An element is just a part of a web page, the kind of element is determined by the tags which open and close it. Not all elements have closing tags, but most do, and all of the basic ones that I'll teach you in this document do.

---

## Basic HTML Structure

So let's start your website! To stay organized, let's create a folder on your computer. It doesn't matter where you make it, but it might be helpful to create it an easily accessible or memorable place so you don't forget where it is or accidentally delete it, like on the desktop or in your documents folder. For now let's just name the folder "website." Now open your favorite text editor. If you don't already have a favorite text editor, a popular editor you could try is Microsoft's [Visual Studio Code.](https://code.visualstudio.com/)

Start a blank new file in your text editor, in VS Code and most other popular editors this can be done by pressing `CTRL+N` on your keyboard. Now that you have a blank file open, you can start writing your html. First, let's write a basic structure that all html-based web pages need:

###### Example 001
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
</head>
<body>
</body>
</html>
```

The code just above is the bare minimum that an html web page needs in order to work correctly. So, what does it mean?

`<!DOCTYPE html>` is a *declaration*, ALL html documents MUST have this declaration as the very first line. This declaration tells the browser, it *declares* to the browser, that it's looking at an html file. When the doctype declaration is not included, sometimes web browsers might switch a weird, non-standard rendering mode that's incompatible with some specifications. Putting the doctype declaration at the start of the file forces the browser to do its best to follow the relevant standard specifications.

`<html lang='en'>`, also called the root element, is the primary html element, all other elements in an html document must be children of the html element. HTML does not technically require an html element to be in the actual structure of an html file, but it's helpful to include the element so that you can specify language through the `lang` attribute. Doing this helps screen readers determine the proper language to use for the web page, thus making your website more accessible for people with vision impairments. In this case, we specified English as the language. If you need a different language code, [here's a list of valid codes.](https://www.w3schools.com/tags/ref_language_codes.asp)

`<head>`, often called the header element, is an element for including metadata about the html document. You can use the header to include information such as the title of the page, a description about what's on the page, the name of the author of the page, and various other things. For the purposes of this guide, we won't really cover all of the metadata that can be included in a header element because it's not necessary to include all of that to learn basic html. The head element is mostly for including metadata for processing by web browsers and other web interfaces, not for humans. In this case we've only included one element in the header.

`<title>` is an element used for declaring the name of your web page. Every page on your website can have its own title, but by default no html document has a title. You have to give it a title if you want it to have one. Whatever you put in the title tag will be what the browser puts in the tab, like up at the top of your browser window in the tab bar. The text after the icon will be whatever the text you put in the title tag. In this case, if someone visited our web page right now, their browser would show a tab called "The title of my website."

`<body>` is where all the content of our page will live. Everything we write and everything we post will go in between `<body>` and `</body>`. In this case, so far there is no content on our web page so the body element is empty. If someone were to visit our web page right now, it would just be a blank, white page.

You can see from this that HTML has a very simple structure, one that's easy to learn and remember. You can imagine it more like a tree if it helps, like this might be another way of visualizing our current web page:

```
- html
    - head
        - title
    - body
```

It's a very simple hierarchy structure, and all you really need to know is the names of these particular elements.

Now, save your file. This can be done in most popular text editors by pressing `CTRL+S`. Save the file as `index.html`. It's very important that the file extension is saved `.html` and not `.txt`! If you put html in a .txt file, it will just be rendered as plain text! It's also important to name the file `index`, on the web the home page of a website is always the file called `index.html`. So, for example, if our website is `reallycoolsite.com` our home page actually lives at `reallycoolsite.com/index.html` but the browser just hides `index.html` from the url.

## Start Putting Content on the page

### Headings and Paragraphs

Now you have the basic html structure, so it's time to actually start putting stuff on the site. For now, let's focus on just some text.

###### Example 002
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
</head>
<body>
    <h1>Welcome to my very cool site!</h1>
    <p>My site is super duper cool!</p>
</body>
</html>
```

Here we've added a heading element and a paragraph element. `<h1>` stands for "heading1" and `<p>` stands for paragraph. Headings change in size depending on the number, for example `<h2>` is smaller than `<h1>` and `<h4>` is *way* smaller! Html supports six levels of headings, so it goes all the way down to `<h6>`!

But, hey, this is all you need to start a website! You now have a functioning web page! Well, you need to actually publish it online first but once you've done that it *will* be a functioning web page.

If you want to add more paragraphs, just add more `<p>` elements:

###### Example 003
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
</head>
<body>
    <h1>Welcome to my very cool site!</h1>
    <p>My site is super duper cool!</p>
    <p>I hope you have a goodd time on my website!</p>
    <p>I love html!</p>
</body>
</html>
```
### Lists

But let's say you want to write a list of something. Like a list of your interests, for example:

- im like vido games
- movies are fun
- i can read

In html you would write this list using `<ul>` (Unordered List) and `<li>` (List Item) elements. For example:

###### Example 004
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
</head>
<body>
    <h1>Welcome to my very cool site!</h1>
    <p>My site is super duper cool!</p>
    <p>I hope you have a goodd time on my website!</p>
    <p>I love html!</p>
    <p>Here are some things I like:</p>
    <ul>
        <li>im like video games</li>
        <li>movies are fun</li>
        <li>i can read</li>
    </ul>
</body>
</html>
```
If you wanted to make a numbered list instead:

1. vibeo gam
2. movies
3. books

You would replace `<ul>` and `</ul>` with `<ol>` and `</ol>` (Ordered List).

### Images

### Links

You'll probably also want to link to other pages at some point. You would do that with the `<a>` element. `<a>` actually stands for anchor, this is called an anchor element. Anchor elements have an attribute called `href` which lets you point to a link. So if I wanted to link to `anothercoolsite.com` I would write an anchor element like this: `<a href='https://anothercoolsite.com/'>Another Cool Site!</a>` You put the url of the page you want to link to in the `href` attribute, enclosed between quotes, and then you write the text you want to be the link inside of the anchor.

So let's get just a bit more complicated.
