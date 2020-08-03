# Document Object Model and Events in JavaScript

This lecture will introduce the Document Object Model (DOM) and event handling system in JavaScript.

### DOM (Document Object Model)
The DOM (Document Object Model) is an API that represents and interacts with any HTML or XML document. The DOM is a document model loaded in the browser and representing the document as a node tree, where each node represents part of the document (e.g. an element, text string, or comment).

The DOM is one of the most-used APIs on the Web because it allows code running in a browser to access and interact with every node in the document. Nodes can be created, moved and changed. Event listeners can be added to nodes and triggered on occurrence of a given event.

- [DOM (Document Object Model](https://developer.mozilla.org/en-US/docs/Glossary/DOM)

### Basic DOM manipulation
The Document Object Model (DOM) is a construct through which web browsers make the HTML structure of a web page (= 'document') available to JavaScript files loaded into that page. We can access the DOM through a global object called document.
Consider this HTML:
```
<body>
  <div id="root"></div>
</body>
```
A common method to access an HTML element through the DOM is by giving it an ID, and then using the document method `getElementById()`.
`const rootDiv = document.getElementById('root');`
Now, we have a reference to the HTML element in our JavaScript code. We can, for instance, set the text content through the innerText property.
`rootDiv.innerText = 'Hello, world!';`
As a result, the HTML structure now looks like this:
```
<body>
  <div id="root">Hello, world!</div>
</body>
```
See the result of what this code changes in this CodePen and play with it yourself.
Note that we are not modifying the HTML file (e.g., index.html) itself. We are just modifying an in-memory representation of the HTML as was initially loaded through the HTML file.
We can also create elements. This creates a button element and sets its label (i.e. innerText), but this in itself is not enough. At this point the button is created but not yet added to the DOM: it is still somewhere "hanging up in the air". We need to attach it to some parent element that is already part of the DOM. This is done by calling `appendChild()` on that parent element, passing it a reference to the newly created element.
`rootDiv.appendChild(myButton);`
As a result, the HTML structure now looks like this:
```
<body>
  <div id="root">
    <button>Click Me!</button>
  </div>
</body>
```
See the result of what this code changes in this CodePen and play with it yourself.
We can set attributes on elements:
`myButton.setAttribute('class', 'my-button');`
Resulting HTML:
```
<body>
  <div id="root">
    <button class="my-button">Click Me!</button>
  </div>
</body>
```
See the result of what this code changes in this CodePen and play with it yourself.
We can add event listeners to elements to respond to user interaction. In this example we are adding an event listener to the button that responds to the click event. This event is triggered whenever the user clicks on the button.
```
 myButton.addEventListener('click', function () {
  const para = document.createElement('p');
  para.innerText = 'You clicked me!';
  rootDiv.appendChild(para);
```

### Events in JavaScript
In Web Applications, we add interactivity through the use of events. Events are “things that happen”, such as mouse clicks, pressing a key on a keyboard, or downloading data via a network request. We add interactivity by “listening” to events on DOM elements. For example, a button would ‘listen’ to a click, and then your program could do something in response to that click, such as displaying a message or altering the state of your application.

### Call Stack
When a function is called it is pushed to the call stack. When a function is finished the function gets shifted from the call stack.
Visualize here: http://latentflip.com/loupe.

## Reading
- [DOM (Document Object Model](https://developer.mozilla.org/en-US/docs/Glossary/DOM)
- [Code Degugging Using the Browser](http://javascript.info/debugging-chrome)
- [Attaching an event](https://www.w3schools.com/jsref/met_element_addeventlistener.asp)

