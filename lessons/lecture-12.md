# APIs II

## React routing

Many modern websites are actually made up of a single page, they just look like multiple pages because they contain components which render like separate pages. These are usually referred to as SPAs - single-page applications. 

What React Router does is conditionally render certain components to display depending on the route being used in the URL (```/``` for the home page, ```/about``` for the about page, etc.).

**Example Create Components**
In this step, we will create four components. The App component will be used as a tab menu. The other three components (Home), (About) and (Contact) are rendered once the route has changed.

```
import React from 'react';
import ReactDOM from 'react-dom';
import { Router, Route, Link, browserHistory, IndexRoute } from 'react-router'

class App extends React.Component {
   render() {
      return (
         <div>
            <ul>
            <li>Home</li>
            <li>About</li>
            <li>Contact</li>
            </ul>
            {this.props.children}
         </div>
      )
   }
}
export default App;

class Home extends React.Component {
   render() {
      return (
         <div>
            <h1>Home...</h1>
         </div>
      )
   }
}
export default Home;

class About extends React.Component {
   render() {
      return (
         <div>
            <h1>About...</h1>
         </div>
      )
   }
}
export default About;

class Contact extends React.Component {
   render() {
      return (
         <div>
            <h1>Contact...</h1>
         </div>
      )
   }
}
export default Contact;

```

## Add a Router
Now, we will add routes to the app. Instead of rendering App element like in the previous example, this time the Router will be rendered. We will also set components for each route.
```
ReactDOM.render((
   <Router history = {browserHistory}>
      <Route path = "/" component = {App}>
         <IndexRoute component = {Home} />
         <Route path = "home" component = {Home} />
         <Route path = "about" component = {About} />
         <Route path = "contact" component = {Contact} />
      </Route>
   </Router>
), document.getElementById('app'))
```
When the app is started, we will see three clickable links that can be used to change the route.


## React Mounting


The React component goes through the following phases
Initialization
Mounting
Update
Unmounting
 
The main job of React is to figure out how to modify the DOM to match what the components want to be rendered on the screen.
 
React does so by "mounting" (adding nodes to the DOM), "unmounting" (removing them from the DOM), and "updating" (making changes to nodes already in the DOM).
How a React node is represented as a DOM node and where and when it appears in the DOM tree is managed by the top-level API.
**React is so fast because it never talks to the DOM directly. React maintains a fast in-memory representation of the DOM.**
However, that in-memory representation is not tied directly to the DOM in the browser (even though it is called Virtual DOM, which is an unfortunate and confusing name for an universal apps framework), and it is just a DOM-like data-structure that represents all the UI components hierarchy and additional meta-data. Virtual DOM is just an implementation detail.
 
Mounting is the process of outputting the virtual representation of a component into the final UI representation (e.g. DOM or Native Components).
 
In a browser that would mean outputting a React Element into an actual DOM element (e.g. an HTML div or li element) in the DOM tree. In a native application that would mean outputting a React element into a native component. You can also write your own renderer and output React components into JSON or XML or even XAML if you have the courage.
 
So, mounting/unmounting handlers are critical to a React application, because you can only be sure a component is output/rendered when it is mounted. However, the componentDidMount handler is invoked only when rendering to an actual UI representation (DOM or Native Components) but not if you are rendering to an HTML string on the server using renderToString, which makes sense, since the component is not actually mounted until it reaches the browser and executes in it.
 
## React Mounting TLDR

Perhaps Mounting is a confusing name. 
componentDidRender and componentWillRender would be much better names.
"Rendering" is any time a function component gets called (or a class-based render method gets called) which returns a set of instructions for creating DOM.
"Mounting" is when React "renders" the component for the first time and actually builds the initial DOM from those instructions.
A "re-render" is when React calls the function component again to get a new set of instructions on an already mounted component.


## React async
 
We've been building things with React so far like to-do and counter apps. When you're pulling in data from an API, then  you're pulling in data for your app. Luckily, React has a solution for situations where you’re handling both data and state.
One way to retrieve data is by using fetch. The usual method of handling data fetching is to:
Make the API call.
Update state using the response if all goes as planned.
Or, in cases where errors are encountered, an error message is displayed to the user.
 
The Fetch API provides an interface for fetching resources. Wether that is to fetch data from a third-party API or fetching data from an API built in-house.
 
There will always be delays when handling requests over the network. That’s just part of the deal when it comes to making a request and waiting for a response. That’s why we often make use of a loading spinner to show the user that the expected response is loading.
 
All these can be done using a library called React Async.
 
React Async is a promised-based library that makes it possible for you to fetch data in your React application. Let’s look at various examples using components, hooks and helpers to see how we can implement loading states when making requests.
 
## React Async Example
 
**Loaders in components**

First, we created a function called ```loadUsers```. This will make the API call using the fetch API. And, when it does, it returns a promise which gets resolved. After that, the needed props are made available to the component.

 
The props are:
- ```isLoading```: This handles cases where the response has not be received from the server yet.
- ```err```: For cases when an error is encountered. You can also rename this to error.
- ```data```: This is the expected data obtained from the server.





## Api Documentation

 
There are certain sections which every good API documentation must have. Without these sections, you will have a hard time understanding how that API can be used.
 
- Authentication. This is the information about authentication schemes your users need to start consuming your API. If you’re using OAuth for example, don’t forget to explain how to set up an OAuth application and securely obtain an API key. 

- Error messages. Error messages are important because you want to get feedback when you’re integrating with your API services in an incorrect way. Explain your error standards, and also provide solutions on how to overcome them when an end consumer gets an error. 

- End points and information on how to consume them. Pay attention to describing your request and response cycles. These are the main components of your API where users will be  interacting with your services, so pay close attention to this.

- Terms of use. This is the legal agreement between the consumer and your organization, defining how the consumer should ideally use your services. This is important because you want to see to it that developers and consumers comply with your organization’s recommended practices, and not do anything that goes against your business values.

- Include API limits under best practices, with terms and conditions. Constraints also need to be clearly stated so that consumers understand what APIs usage and practices are permitted. 

- Change log. Detail updates and versions of your APIs and how that might affect API consumers. This will help consumers know the stability of your API and see if any changes need to be made for an effective API call. Once you’ve listed these sections, it’s easy to go about documenting them, because now your API is already off to a great start.


## Reading

- [React Router Artice](https://www.tutorialspoint.com/reactjs/reactjs_router.htm)
- [React Router Primer](https://www.freecodecamp.org/news/react-router-in-5-minutes/)
- [Mount vs Render](https://reacttraining.com/blog/mount-vs-render/)
- [Lifecycle](https://www.w3schools.com/react/react_lifecycle.asp)
- [Lifecycle Deep Dive](https://hackernoon.com/reactjs-component-lifecycle-methods-a-deep-dive-38275d9d13c0)
- [React Async](https://css-tricks.com/fetching-data-in-react-using-react-async/)



