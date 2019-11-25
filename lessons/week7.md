# HTML and CSS Preliminaries, Forms and Data Validation

## Agenda

1. Introduction to CSS:
   - Crash course
   - Where to write it?
   - The box model
   - The cascading effect


## 1. Introduction to CSS

### Crash course

CSS is just as important as HTML. It is an acronym for **Cascading Style Sheets**. It is a language created to change the appearance of content. By referring to the HTML tags you can `style` it in various ways: change the font size, increase the height or attach a background image to it.

Go through the following video to get a firmer foundation:

- [CSS Crash Course](https://www.youtube.com/watch?v=yfoY53QXEnI)

### Where to write it?

There are 3 basic ways to write CSS:

- In an external stylesheet: a `.css` file, that is linked to a `.html` file.
- In the <head> of a `.html` file. This is done using the `<style>` tag.
- As part of the attribute `style` inside any HTML tag.

In practice, you'll always write your CSS in separate `.css` files. This is because you want to make sure **every file has a single purpose**: an HTML file should only contain the content and structure of a page, while a stylesheet should only contain styling rules that apply to a page.

### The box model

"In CSS, everything is a box". This phrase summarizes a central concept in HTML/CSS: the box model. When building a web page each element can be considered a box that has the following properties: `margins`, `borders`, `paddings` and `content`. Starting from the first element within the <body>, everything that comes after will be pushed down (thanks to these 4 properties).

Watch the following video to [learn more](https://www.youtube.com/watch?v=rIO5326FgPE).
Read the following article to [learn more](https://learn.shayhowe.com/html-css/opening-the-box-model/).

### The cascading effect

The first C in CSS stands for Cascading and it's crucial to learning how to use CSS correctly. Essentially, it means that it matters
(1) **in which order** and
(2) **how specific**
you write CSS rules.

Read the following articles to learn about it:

- [The "C" in CSS](https://css-tricks.com/the-c-in-css-the-cascade/).
- [How CSS works: understanding the cascade](https://blog.logrocket.com/how-css-works-understanding-the-cascade-d181cd89a4d8)



## Reading

## Additional Reading
