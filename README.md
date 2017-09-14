# React State Management - Redux and React-Redux

## Prerequisites

1. Competent with modern JavaScript (ES6+) & React
2. Familiar with the practice of 'lifting state'
3. Understanding of the concept of immutability

## Why, Why, Why (another library)?

React excels at allowing you to divide your user interface into modular, reusable components. Each component renders a portion of the user interface based on its state and props. You can think of a component (or its render method) as a function that takes as its input some props (or some props and state) and outputs a portion of the DOM. Data in, data out. React lets you, as the docs say, "build encapsulated components that manage their own state." So what's the problem?

_Understanding why you might need Redux is as, if not more important, than knowing how to use Redux..._

### State Management!

Even though components can manage their own state, React is not very opinionated when it comes to the question: How do you manage state that is shared across components? There are a variety of ways to do so including:

1. Lifting state: you've likely encountered this state management pattern when learning pure React. The [React docs](https://facebook.github.io/react/docs/lifting-state-up.html) have a great section on how to do it effectively. You should get into the habit of doing this to manage shared state _until it becomes unwieldy, unscalable, or developer unfriendly._ This is important, you don't want to use state management alternatives until you need to... unless you're exploring the  library for learning purposes.
2. Using context: [Context](https://facebook.github.io/react/docs/context.html) is a somewhat obscure portion of React's API. Lots of popular libraries like Redux and React Router use it under the hood, but you should avoid it. Lift state until you need a better alternative, then use one of the third-party alternatives.
3. [Redux](http://redux.js.org/): duh.
4. [MobX](https://mobx.js.org/index.html): another popular React state management solution that employs functional reactive programming.

### Important caveats

1. You don't need to use Redux _with_ React, you can use it with any view library, or none.
2. Just like with lifting state, you don't need to put _all_ of your components' state objects in Redux. A good use case for Redux is a logged-in user object, the properties of which will likely need to be accessed all over the place. A bad use case for Redux would be a boolean property, e.g. `isValid`, according to which you conditionally render a password input field's background color as either green or red.
3. You can use just Redux with React, but it is most commonly used with a binding library called, aptly, React Redux, that makes it a bit easier to use.
4. This tutorial is intended to _introduce_ the basic concepts of Redux. To fully understand and appreciate the library you'll need to put in some time with its excellent documentation along with the following resources:
    - [Redux video tutorial by one of Redux's creators](https://egghead.io/courses/getting-started-with-redux)
    - [Intermediate Redux video series, also by one of its creators](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)

