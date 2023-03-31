# learn css

## Introduction

CSS, like html, is a very simple coding language and it's very easy to learn. Once you understand html structure, you're very well on your way to understanding css as well! This is because css just applies style properties to elements in the html. HTML tells the browser how to format content on a page, and CSS tells the browser what properties the HTML should have.

For example, in our [basic HTML tutorial](html.md) we discussed HTML structure, the `<body>` tag and the `<p>` tag. We can customize the way these elements look using CSS! If we wanted to make our web page white text on a black background, and adjust the positioning of our paragraph elements so that they had a thick margin on both their left and right sides so they'd appear as blocks of text in the middle of the screen, we could write CSS that looks something like this:

###### Example 001
```css
body {
    display: flex;
    color: white;
    background-color: black;
}
p {
    max-width: 45em;
    margin: auto;
}
```

<style>
    p.ex1 {
        padding: 10px;
        text-align: center;
        color: white;
        background-color: black;
    }
</style>
<p class=ex1>The result of that css would look something like this!</p>

What does this code actually do?

`body` tells the browser that the following style declaration block will be applied to the `<body>` element in the html. We use the `display` property to tell the browser that the body element should act as a flexbox container. And the properties `color` and `background-color` are probably pretty self-explanatory, they tell the browser what colors to use to display the body element. In this case, we set the background to black and the text to white.

Then we start a new rule set for `<p>` elements and we tell the browser that they should not ever be wider than `45em` by using the `max-width` (maximum width) property. An `em` is a measurement unit in CSS, it scales relative to the font size of the element it's used in. You can also use `px` which is an exact pixel measurement, `%` which scales relative to the parent element, `rem` which scales relative to the root element, and a few others. We also tell the browser to automatically calculate the best margins for paragraph elements, and because we set the body element, which is the parent of our paragraph elements, to be a flexbox, auto margins centers paragraphs!

Explaining the details of what a flexbox is or how to use flexboxes to their full potential is unfortunately outside of the scope of this project, but [you can read more about it here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) if you'd like to.
