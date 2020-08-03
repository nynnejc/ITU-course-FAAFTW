# React Part II

## Building components
- Stateful logic - Having logic around state.

### Create react app
- Create react app. https://github.com/facebook/create-react-app
- How to run npm run start.

### Component tree
### Stateful logic
- Using destructuring in React
- State vs. Props
Both props and state trigger a render update when they change
- How to determine if data should be props or state? Props are "configuration options" for components. State is completely optional. State increases complexity and reduces predictability. Use props unless you definitely need to use state. State is single-level only. Components can read and set their own state, but cannot read or set the state of their children.

### Using state correctly
- Do not modify state directly, always use setState.
- Give an example of how mutating state directly doesn’t work. State updates are merged (note that merging is shallow). setState is an asynchronously-executed request to change state.

### List keys. 
- Render list first without adding the key. See the error. Assignment of unique key to every item rendered in an array. Keys help React identify which items have changed, are added, or are removed.

### Lifecycle Methods.
- Lifecycle methods are used when render is not enough on its own.
- componentDidMount: data fetching in client-side-only apps
- shouldComponentUpdate: performance debugging
- componentWillUnmount: teardown (payment SDKs, intervals, etc)

Question: in which of these lifecycle methods is it OK to call setState? (watch out for stack overflows)
Code inspiration
todolist (updating state with list)
https://codesandbox.io/s/simple-todo-list-be9qu
 

## Reading

- [Forms in React](https://reactjs.org/docs/forms.html)
- [Typechecking with Proptypes](https://reactjs.org/docs/typechecking-with-proptypes.html)
- [Props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)
- [Context](https://reactjs.org/docs/context.html)
- [Render Props](https://reactjs.org/docs/render-props.html)
- [Refs and the DOM](https://reactjs.org/docs/refs-and-the-dom.html)
