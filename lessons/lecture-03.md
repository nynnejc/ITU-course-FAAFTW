# HTML and CSS Preliminaries, Forms and Data Validation

In this lecture, we'll introduce structural and semantic HTML elements, their role in creating layout and describing the content of Web pages, and an introduction to CSS including the use of selectors, CSS specificity and typography. The lecture will also provide an introduction to form elements that allow users to input data and interact with Web pages.

## Introduction to CSS

CSS, or **Cascading Style Sheets** is a language created to change the appearance of content. By referring to the HTML tags you can `style` it in various ways: change the font size, increase the height or attach a background image to it.

### Where to write it?

There are 3 basic ways to write CSS:

- In an external stylesheet: a `.css` file, that is linked to a `.html` file.
- In the <head> of a `.html` file. This is done using the `<style>` tag.
- As part of the attribute `style` inside any HTML tag.

In practice, you'll always write your CSS in separate `.css` files. This is because you want to make sure **every file has a single purpose**: an HTML file should only contain the content and structure of a page, while a stylesheet should only contain styling rules that apply to a page.

### The box model

"In CSS, everything is a box". This phrase summarizes a central concept in HTML/CSS: the box model. When building a web page each element can be considered a box that has the following properties: `margins`, `borders`, `paddings` and `content`. Starting from the first element within the <body>, everything that comes after will be pushed down (thanks to these 4 properties).

- [The box model](https://learn.shayhowe.com/html-css/opening-the-box-model/).

### The cascading effect

The first C in CSS stands for Cascading and it's crucial to learning how to use CSS correctly. Essentially, it means that it matters
(1) **in which order** and
(2) **how specific**
you write CSS rules.

Read the following articles to learn about it:

- [The "C" in CSS](https://css-tricks.com/the-c-in-css-the-cascade/).
- [How CSS works: understanding the cascade](https://blog.logrocket.com/how-css-works-understanding-the-cascade-d181cd89a4d8)

## Forms
Forms are a useful and familiar tool to interact with your users.
- [Forms](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Your_first_HTML_form)

### Forms Validation
Beware of form validation! As a rule, users will think of creative ways to misuse your product wether by malice or mistace that you can hardly think of. Form validation to the rescue.
- [Forms validation](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation)

## Class Material
- [Box model](https://learn.shayhowe.com/html-css/opening-the-box-model/)
- [The "C" in CSS](https://css-tricks.com/the-c-in-css-the-cascade/).
- [How CSS works: understanding the cascade](https://blog.logrocket.com/how-css-works-understanding-the-cascade-d181cd89a4d8)
- [Forms](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Your_first_HTML_form)
- [Forms validation](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation)


## Additional Material
