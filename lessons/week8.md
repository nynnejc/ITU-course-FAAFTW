# CSS Layout and Positioning, Responsive Design


## More advanced CSS

By now you've had some practice with CSS. In the following sections you'll learn about some more essentials concepts in order to write modern stylesheets for the web!

### Flexible organizing with flexbox

CSS is used to order and style HTML elements. A big part of this is organising elements in a visually attractive way. This can be done using Flexbox.

What it does is helping you to think according to 'grid-based web design': elements are not randomly placed on the page, but are neatly organised along a grid.

Read the following to learn more about 'grid-based web design':

- [Introduction to grids in web design](https://webdesign.tutsplus.com/articles/a-comprehensive-introduction-to-grids-in-web-design--cms-26521)
- [Intro to Web Design Grids](https://www.youtube.com/watch?v=gjYZoPEk0ow)

Once you understand this way of thinking you'll know why it makes sense to know Flexbox.

In order to make use of it we have to access it through the `display` CSS property:

```css
display: flex;
```

This will give us the Flexbox-specific properties, so we can develop clean and organised CSS. Check the following links to understand how this is done:

- [CSS Flexbox Course](https://www.youtube.com/watch?v=-Wlt8NRtOpo)
- [CSS Flexbox Tutorial for Beginners 1/2 ](https://www.youtube.com/watch?v=siKKg8Y_tQY)

### Pseudo class selectors

Every HTML element can be in different states. The default state is when an element is untouched. You already know how to style for this.

```css
p {
  color: white;
}
```

There are times when a user interacts with an element. For example: clicking a button that opens another page. As frontend developers we need to give the user feedback on that particular action. When they place the mouse on top of the button it lights up (we call this a `hover state`). We need to write instructions for that to happen.

Like the hover state there are others as well: click, focus, visited, and others. For most of these element states we have special selectors. Read the following article to learn about them. Once you do try the out for yourself!:

- [Pseudo class selectors](https://css-tricks.com/pseudo-class-selectors/)

### Responsive design with media queries

Nowadays people use different devices to access websites: desktops, tablets and mobile phones of all different sizes. Responsive design is a way to put together a website so that it automatically scales its content and elements to match the screen size of the viewer. It prevents that images are larger than the screen width, so visitors on mobile devices will see a visually attractive website as well

For more information about responsive design, check this article: [Responsive Design](https://internetingishard.com/html-and-css/responsive-design/).

The primary way of making a responsive website is by writing custom CSS code that makes it so. This can be done using `media queries`: CSS instructions that only apply to certain screen sizes.

Start reading about media queries here: [Introduction to Media Queries](https://varvy.com/mobile/media-queries.html).

## Reading

## Additional Reading
