# learn css

## Repo Navigation

| Learn:                          | Resources:                         | About:
| ------------------------------- | ---------------------------------- | ---------------------------------------------
| - [HTML](html.md)        | - [Templates](../templates/readme.md) | - [Home/Introduction](../)
| - [CSS](css.md)          | - [Builders](builders.md)   | - [Mission Statement](../mission-statement.md)
| - [Dictionary](vocab.md) | - [Hosts](hosts.md)         | - [View on Github](https://github.com/skylestia/make-a-website)

---

Table of Contents

- [learn css](#learn-css)
  - [Repo Navigation](#repo-navigation)
  - [Introduction](#introduction)
  - [Add css to your html](#add-css-to-your-html)
  - [Centering a div](#centering-a-div)
  - [CSS Inheritance](#css-inheritance)
  - [Conclusion](#conclusion)


---

## Introduction

CSS, like html, is a very simple coding language and it's very easy to learn. Once you understand html structure, you're very well on your way to understanding css as well! This is because css just applies style properties to elements in the html. HTML tells the browser how to format content on a page, and CSS tells the browser what properties the HTML should have.

For example, in our [basic HTML tutorial](html.md) we discussed HTML structure, the `<body>` tag and the `<p>` tag. We can customize the way these elements look using CSS! If we wanted to make our web page white text on a black background, the CSS would very simply be:

###### Example 001
```css
body {
    color: white;
    background-color: black;
}
```

What does this code actually do?

`body` tells the browser that the following style declaration block will be applied to the `<body>` element in the html. We use the `color` property to set the text color to white and we use the `background-color` property to set the background of the body element to black.

There are various other properties that can be applied to elements as well. Some common ones include:

`margin` - adjusts the margins of an element.

`width` - adjusts the width of an element.

`font-size` - adjusts the font size of an element.

`display` - adjusts how an element is displayed in the flow

You must put all rules in css between curly brackets: `{}` and you must end each rule with a semicolon: `;`. In the above example there are two rules and one ruleset. `body` and all the properties defined between the curly brackets is a ruleset. Each property defined in the ruleset is a rule. In other words, `color: white;` is a rule, where `color` is the property and `white` is the value. `background-color: black;` is the other rule, where `background-color` is the property and `black` is the value.

One very important thing you will also need to know about CSS is that styles lower in the document have greater priority than styles higher in the document. Styles in a CSS file *cascade,* hence the name: "cascading stylesheets." This means that if `body` is set to `margin: auto;` at the top of the document but it's set to `margin: 15em;` at the bottom of the document, then the CSS will use `margin: 15em;` for the body element.

---

## Add css to your html

Start by creating a new file in the same folder as your html, name it something like `style.css`. So if you named your folder `website` like in the html tutorial, your folder should now contain both an `index.html` file and a `style.css` file. Unlike the html file, it doesn't actually matter what you name your `css` file *as long as* the file uses a `.css` file extension.

Once your file is created, go back to your `index.html` and add a new line in your `<head></head>` element. Create an external resource `link` element on that new line. An external resource link element looks like this: `<link rel="" href="">`. Link elements do not have closing tags! We'll use this element to include your `style.css` file! The `rel` attribute tells the browser what kind of resource it is and the `href` attribute tells the browser where the resource is located. In this case the resource is a stylesheet and the resource is located in the same folder as the html. So you'd write the link element like this:

`<link rel="stylesheet" href="style.css">`

Putting this element inside of your `head` element will include your css in your html!

---

## Centering a div

One very common issue that people face when making a website is centering their primary div. It's actually very simple to do, but if you're new to css it may not be obvious or intuitive.

Let's continue with our html from the html tutorial:

###### Example 002
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Welcome to my very cool site!</h1>
    <p>My site is super duper cool!</p>
    <p>I hope you have a good time on my website!</p>
    <p>I love html!</p>
    <p>Here are some things I like:</p>
    <ul>
        <li>im like video games</li>
        <li>movies are fun</li>
        <li>i can read</li>
    </ul>
    <p>You can check out another super cool website I really like by <a href='https://anothercoolsite.com/'>clickin here!</a>
    <img src='images/construction.gif'>
</body>
</html>
```

Let's wrap our content in one primary `div` element. We'll give it a class so that we can style it separately from other divs, we'll call it `wrapper`:

###### Example 003
```html
<!DOCTYPE html>
<html lang='en'>
<head>
    <title>The title of my website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="wrapper">
        <h1>Welcome to my very cool site!</h1>
        <p>My site is super duper cool!</p>
        <p>I hope you have a good time on my website!</p>
        <p>I love html!</p>
        <p>Here are some things I like:</p>
        <ul>
            <li>im like video games</li>
            <li>movies are fun</li>
            <li>i can read</li>
        </ul>
        <p>You can check out another super cool website I really like by <a href='https://anothercoolsite.com/'>clickin here!</a>
        <img src='images/construction.gif'>
    </div>
</body>
</html>
```

Now lets use css to specify a width to the `.wrapper` container and add margins to it. We want the wrapper to be a width comfortable to read in, so not too wide but not too thin. In my experience, generally something between `30em` and `45em` is pretty ideal on desktop devices. But it would also be preferably if the width adjusted to be able to fit comfortable on a mobile screen as well, so we'll use the `max-width` property instead of the `width` property. Open up the `style.css` file and create a ruleset for the wrapper element, then add rules for `max-width` and `margin`.

###### Example 004
```css
.wrapper {
    max-width: 40em;
    margin: auto;
}
```

Setting `margin` to `auto` is what's really key here. As long the element has a width, an automatic margin will center the element relative to its parent element. In this case, the parent of `.wrapper` is the body element, which defaults to having a width the size of the screen, so setting auto margin on `.wrapper` centers the wrapper element on the screen. You can also manually adjust the margin by doing something like this: `margin: 15em;` This will set margins on all side of the element to `15em`. You can set margins of individual sides of the element by instead using the properties: `margin-top`, `margin-right`, `margin-bottom`, and `margin-left`. These properties can also all be set with the regular `margin` property with shorthand. Like this: `margin: top right bottom left`. For example, `margin: 50px 150px 80px 200px;` translates to:

```css
margin-top: 50px;
margin-right: 150px;
margin-bottom: 80px;
margin-left: 200px;
```

---

## CSS Inheritance

In CSS, elements that are the children of other elements in the HTML structure will inherit the styles of their parents. In this case, `.wrapper` is the child of `body` so `.wrapper` will inherit styles from `body`. If we used css to make our page white text on a black background as in [example 001](#example-001), then the wrapper element in our html will also have white text on a black background. Every element contained in `body` will inherit those styles, so it's not necessary to re-specify those colors for other elements. So our CSS could look like this:

###### Example 005
```css
body {
    color: white;
    background-color: black;
}
.wrapper {
    max-width: 40em;
    margin: auto;
}
```

And our entire page will be white text on a black background.

---

## Conclusion

I don't really know what else to explain to teach you CSS, this will already be enough for most simple, static personal websites. If you have any specific questions feel free to create a new post in the [Q&A category in this repo's Discussions](https://github.com/skylestia/make-a-website/discussions/categories/q-a) and ask!

This tutorial might also be updated in the future as I think of things to add, but HTML is really the main focus of this repo.

Otherwise, you can learn more CSS on your own:

- [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3 Schools](https://www.w3schools.com/w3css/defaulT.asp)
- [Codecademy](https://www.codecademy.com/learn/learn-css)
- [Web.dev](https://web.dev/learn/css/)