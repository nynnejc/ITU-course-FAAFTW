# CSS Layout and Positioning, Responsive Design

This lecture provides a more in-depth focus on how to use CSS to implement your designs and layout content on the Web and introduces the concept of the CSS box model and the use of different positioning schemes. It also provides an introduction to the various responsive design strategies used to ensure that content on the Web is viewable on all devices - both desktop and mobile - and introduces Bootstrap: a column-based CSS framework for laying out content on the Web.
  
## CSS Frameworks

A CSS framework allows you to style your HTML reliably, by making use of pre-defined CSS rules. This way you don't have to think about what custom CSS you have to write to make something the way you want. This is useful mainly to speed up development.

There are other reasons as well which you can learn about in teh following article:

- [What are the benefits of using a CSS framework](https://css-tricks.com/what-are-the-benefits-of-using-a-css-framework/)

### Most popular frameworks

There are a lot of different CSS frameworks out, each with their pros and cons. In the following video you'll learn about several of the top ones used and what problems exactly they're trying to solve:

- [CSS frameworks](https://www.youtube.com/watch?v=AMDx0IIgiK4)

### Framework vs. custom

As a general rule, you always want to be able to write custom CSS when needed. And if you're using a framework, you at least know why it works the way it does. This means that you look into the class definition within the stylesheet (you can use the browser inspector for this, more on that later).

However, writing custom CSS is in practice not always possible. This could be because of project deadlines, lack of skill or wanting to do rapid prototyping (a technique to quickly build a working version in order to test if it works). This is when we use frameworks to help us out.

Keep in mind that a framework should be there only to assist, not compensate. Research the following resources to learn about the pros and cons of CSS frameworks:

- [Are CSS Frameworks Bad?](https://www.youtube.com/watch?v=VlY5CfkL760)
- [Discussing the Pros and Cons of Using a CSS Framework](https://speckyboy.com/discussing-the-pros-and-cons-of-using-a-css-framework/)

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

## Class Material

- [What are the benefits of using a CSS framework](https://css-tricks.com/what-are-the-benefits-of-using-a-css-framework/)
- [CSS frameworks](https://www.youtube.com/watch?v=AMDx0IIgiK4)
- [Are CSS Frameworks Bad?](https://www.youtube.com/watch?v=VlY5CfkL760)
- [Discussing the Pros and Cons of Using a CSS Framework](https://speckyboy.com/discussing-the-pros-and-cons-of-using-a-css-framework/)
- [Introduction to grids in web design](https://webdesign.tutsplus.com/articles/a-comprehensive-introduction-to-grids-in-web-design--cms-26521)
- [Intro to Web Design Grids](https://www.youtube.com/watch?v=gjYZoPEk0ow)
- [CSS Flexbox Course](https://www.youtube.com/watch?v=-Wlt8NRtOpo)
- [CSS Flexbox Tutorial for Beginners 1/2 ](https://www.youtube.com/watch?v=siKKg8Y_tQY)
- [Pseudo class selectors](https://css-tricks.com/pseudo-class-selectors/)


## Additional Material

## Working with the browser

### What is a web browser?

You probably use it daily. Let's take a closer look at what it actually is.

A web browser is software that allows you view webpages, either retrieved from the internet or loaded from your computer. The primary function of a web browser is to render HTML files, transforming all the code (HTML, CSS and JavaScript) as well as the references (images, videos, etc.) to display a page.

For further study, watch the following:

- [What is a browser?](https://www.youtube.com/watch?v=TcbhVv9ty44)
- [How web browsers work](https://www.youtube.com/watch?v=WjDrMKZWCt0)

Read:

- [About your web browser](http://www.allaboutcookies.org/browsers/)

### Choosing the right browser

As a web developer you will write code that will display in browsers. As such it is important that you get familiar with most major browsers in use today. These are:

- [Internet Explorer](https://support.microsoft.com/en-us/help/17621/internet-explorer-downloads)
- [Google Chrome](https://www.google.com/chrome/)
- [Safari](https://support.apple.com/downloads/safari)
- [Mozilla Firefox](https://www.mozilla.org/en-GB/firefox/new/)
- [Microsoft Edge](https://www.microsoft.com/en-us/windows/microsoft-edge) (Not available for Mac/Linux yet)
- [Opera](https://www.opera.com/download)

In your HackYourFuture journey you'll mainly be using **Google Chrome** when developing, as is has great developer tools that allow us to develop web applications in an easy and clear way.

### How to use the browser inspector :mag:

The inspector is part of browsers developers can use to take a closer look at the composition of the HTML elements. This makes it easier to write correct HTML and CSS code that works.

Watch the following video and follow along:

- [Google Chrome Developer Tools Crash Course](https://www.youtube.com/watch?v=x4q86IjJFag)

### Useful browser extensions

As web developers we'll be dealing with the browser all the time. Why not upgrade our browser so it can make our programming life easier?

A `browser extension` is a piece of software someone has written to increase the capability of the browser. For example, if you hate receiving advertisements you probably use something like [Adblock](https://chrome.google.com/webstore/detail/adblock/gighmmpiobklfepjocnamgkkbiglidom) to block all the unwanted ads you might find in your webpages (if not, download it as soon as possible!).

The following is a list of extensions that have proven to be useful during development. This list only applies for Google Chrome, so if you don't have it [install it](https://www.google.com/chrome/).

Extensions:

- Modify the technologies underlying each website, in real time, using [Web developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm/related?hl=en-US)
- Expose what technologies a website is using with [WhatRuns](https://chrome.google.com/webstore/detail/whatruns/cmkdbmfndkfgebldhnkbfhlneefdaaip?hl=en-US)
- If oyu ever wanted to know the exact color of any element in a page, you can now do so with [ColorZilla](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=en-US)
- When developing you'll be using dummy text to populate your elements. Enter [Loren Ipsum Generator](https://chrome.google.com/webstore/detail/lorem-ipsum-generator-def/mcdcbjjoakogbcopinefncmkcamnfkdb?hl=en%20)

There are many moreof these extensions and we encourage you to explore. See what fits your needs!
