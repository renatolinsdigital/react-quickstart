# React quickstart - Essential notes by Renato Lins  

React was initially created by Jordan Walke, a software engineer at Facebook, and released as an open-source project in 2013. React's purpose is to enable efficient and dynamic user interface (UI) development for web applications by leveraging a component-based architecture and a virtual DOM. With its declarative syntax and unidirectional data flow, React has become one of the most popular JavaScript libraries for building fast, scalable, and maintainable front-end applications. Since its release, React has evolved to power modern web development, being widely adopted by developers and major companies worldwide.

## Table of contents 

????????????????

---

### 1. Considerations about React  

Learning React can significantly enhance your front-end development skills and career opportunities in the tech industry. Its widespread adoption, active community, and integration with modern tools make React a highly sought-after skill for building web and mobile applications. Mastering React opens doors to opportunities in UI/UX development, single-page applications (SPAs), mobile app development (via React Native), and server-side rendering (SSR). React's simplicity, flexibility, and ecosystem position it as a cornerstone for developers in the ever-evolving front-end landscape. Key Features of React:

__Component-Based Architecture__: React allows developers to break UIs into modular, reusable components. Each component manages its logic and presentation, making codebases more maintainable and scalable.

__Virtual DOM__: React uses a virtual DOM to optimize UI updates. Changes are first made in a lightweight virtual representation of the DOM, and React calculates the minimal set of updates needed to reflect changes in the actual DOM, improving performance.

__Declarative Syntax__: React provides a declarative way to build UIs. Developers describe what the UI should look like, and React takes care of updating the DOM based on state changes, reducing complexity.

__Unidirectional Data Flow__: React enforces a unidirectional data flow, where data flows from parent components to child components. This makes state management predictable and debugging easier.

---

### 2. React Architecture and Ecosystem Overview  

Understanding React’s core architecture and its ecosystem is essential for building efficient and scalable applications. React’s architecture focuses on the foundational concepts and tools that power the library, while its ecosystem includes additional tools and libraries that enhance development. So we can consider:

**Core Architecture:**

__Components__: Components are the building blocks of React applications. They can be functional or class-based and encapsulate both UI and logic. Components can accept input via props and manage internal state.  

__State and Props__:  
- __State__: State represents data or variables that may change over time and trigger UI updates. Components use state to manage dynamic content.  
- __Props__: Props (properties) allow data to be passed from parent components to child components, enabling dynamic and reusable components.  

__Virtual DOM__: React minimizes direct manipulation of the real DOM by using a virtual DOM. Changes are made to this lightweight representation first, and React determines the minimal set of updates needed to sync it with the real DOM.  

__Reconciliation__: React’s reconciliation algorithm efficiently compares the previous and new virtual DOM trees, ensuring that only necessary updates are applied to the real DOM.  

__Hooks__: Introduced in React 16.8, hooks enable components to use state, lifecycle methods, and side effects without needing classes. Key hooks include:  
- `useState`: Manages state in functional components.  
- `useEffect`: Handles side effects like API calls and DOM manipulation.  
- `useContext`: Provides global state without prop drilling.  

__React Lifecycle__: React components have lifecycle phases: mounting, updating, and unmounting. Class components use lifecycle methods like `componentDidMount`, while functional components achieve the same functionality with hooks like `useEffect`.  

__JSX__: JSX allows developers to write HTML-like syntax within JavaScript. It is transpiled into React `createElement` calls using tools like Babel, bridging markup and logic seamlessly.  

__React Fiber__: React Fiber, introduced in React 16, optimizes rendering by breaking work into smaller incremental units, enabling better task prioritization and smoother UI updates.  

__Context API__: Provides a built-in solution for sharing state across components without prop drilling, improving code readability and maintainability.  

__React DOM__: React DOM handles rendering React components in the browser, bridging the virtual DOM and the real DOM for efficient updates and rendering.  

**React Ecosystem:**

__React Router__: A library for managing navigation and routing in React applications, enabling seamless single-page application (SPA) behavior and dynamic content loading.  

__React Native__: Extends React to mobile development, allowing cross-platform mobile apps for iOS and Android using JavaScript and React’s component-based architecture.  

__State Management__: Libraries like Redux, Zustand, or Recoil complement React’s built-in state to manage complex application state more effectively.  

__Next.js__: A framework for server-side rendering (SSR) and static site generation (SSG), providing features like file-based routing, API routes, and performance optimizations for scalable applications.  

__Styled Components__: A CSS-in-JS library for writing component-scoped styles. It supports dynamic styling via props, theming, and server-side rendering compatibility.  

__Tooling__: React integrates with tools like Webpack, Babel, and ESLint, supporting optimizations like code splitting, lazy loading, and performance monitoring via React DevTools.  

__React Testing Library__: A testing tool that, along with Jest, ensures components render and behave as expected, promoting robust testing practices.  

---

### 3. Essential JavaScript Knowledge Before Coding with React  

React is a JavaScript framework designed to solve common problems in building user interfaces, such as efficiently updating the DOM and managing state. Since React is built on top of JavaScript, having a solid understanding of the language's fundamentals is essential to use React effectively. Knowing the basics of JavaScript will help you better grasp React's concepts and enable you to write clean, maintainable code. Below are key JavaScript concepts you should master before diving into React.

**1. Data Types**

```javascript
let num = 42;          // Number
let str = "Hello";     // String
let bool = true;       // Boolean
let arr = [1, 2, 3];   // Array
let obj = { key: "value" }; // Object
let nothing = null;    // Null
let undef;             // Undefined
```

**2. Arrow Functions**

```javascript
// Arrow Function
const add = (a, b) => a + b;  
console.log(add(2, 3)); // 5  
```

**3. Template Strings**

```javascript
const name = "John";
console.log(`Hello, ${name}!`); // Hello, John!
```

**4. Essential Array Methods**  

- **`map`**:  

```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(n => n * 2);
console.log(doubled); // [2, 4, 6]
```

- **`filter`**:

```javascript
const numbers = [1, 2, 3, 4];
const evens = numbers.filter(n => n % 2 === 0);
console.log(evens); // [2, 4]
```

- **`find`**:

```javascript
const numbers = [1, 2, 3];
const found = numbers.find(n => n > 2);
console.log(found); // 3
```

- **`forEach`**:

```javascript
[1, 2, 3].forEach(n => console.log(n));
// 1
// 2
// 3
```

**5. Destructuring and Spread/Rest Operators**  

- **Destructuring**:

```javascript
const person = { name: "Alice", age: 25 };
const { name, age } = person;
console.log(name, age); // Alice 25

const [first, second] = [1, 2, 3];
console.log(first, second); // 1 2
```

- **Spread Operator**:

```javascript
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // [1, 2, 3, 4]
```

- **Rest Operator**:

```javascript
const [first, ...rest] = [1, 2, 3, 4];
console.log(rest); // [2, 3, 4]
```

**6. Classes and Objects**  

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

const john = new Person("John", 30);
john.greet(); // Hello, my name is John.
```

**7. Modules and Imports**  

- **Exporting**:  

```javascript
// math.js
export const add = (a, b) => a + b;
```

- **Importing**:  

```javascript
import { add } from './math.js';
console.log(add(2, 3)); // 5
```

**8. Promises + Async/Await**  

- **Promises**:  

```javascript
const fetchData = () => {
  return new Promise((resolve) => setTimeout(() => resolve("Data loaded"), 1000));
};

fetchData().then(result => console.log(result)); // Data loaded
```

- **Async/Await**:  

```javascript
const fetchData = async () => {
  const result = await new Promise(resolve => setTimeout(() => resolve("Data loaded"), 1000));
  console.log(result);
};

fetchData(); // Data loaded
```

**9. Immutability**  

- **Immutable Array Update**:  

```javascript
const numbers = [1, 2, 3];
// Add a new item
const newNumbers = [...numbers, 4]; 
console.log(newNumbers); // [1, 2, 3, 4]
```

- **Immutable Object Update**:  

```javascript
const person = { name: "Alice", age: 25 };
// Update age
const updatedPerson = { ...person, age: 26 };
console.log(updatedPerson); // { name: "Alice", age: 26 }
```

---

### 4. Getting Started with React + Vite  

Starting with React can seem overwhelming due to the variety of tools and frameworks available today. However, the key is to begin with a simple setup that focuses on React's core concepts without introducing unnecessary complexity. In the past, developers commonly used **Create React App (CRA)** to bootstrap React projects. While it provided an easy way to get started, CRA is no longer recommended due to its slower build times and lack of modern optimizations. Frameworks like **Next.js** offer powerful features such as server-side rendering (SSR) and static site generation (SSG), which are excellent for production applications. However, Next.js introduces many new concepts that are not core to React, like file-based routing and API routes. This added complexity can overwhelm beginners who are still learning the basics of React.  

**Vite – An easy Way to Start**

A modern and lightweight alternative to CRA is **Vite**. Vite provides a very fast development experience, optimized build times, and an easy setup process. It’s a great tool to start with React while maintaining flexibility.  

**Step-by-Step: Setting Up React with Vite**  

1. **Install Node.js**  

Ensure you have Node.js installed. Check by running:  

```bash
node -v
npm -v
```

2. **Create a New React Project with Vite**  

Run the following commands in your terminal:  

```bash
npm create vite@latest my-react-app --template react
cd my-react-app
npm install
```

You'll be prompted to select features. You can simply choose **React** and **JavaScript**.

__NOTE:__ While TypeScript can enhance projects (and is highly recommended), this guide will focus on React without TypeScript for simplicity.

3. **Start the Development Server**  

Run the project locally:  

```bash
npm run dev
```
This will start a development server, and you can access your React app at `http://localhost:5173`. You'll be presented with a sample application, which you can clean, adapt, enhance, etc. Typically, developers begin with a 'cleanup' phase, where they remove everything unnecessary before starting to code.

**Writing Your First React Component**  

Inside `src/App.jsx`, replace the content with the following:  

```jsx
function App() {
  return (
    <div>
      <h1>Hello, React!</h1>
      <p>Let's start building awesome apps.</p>
    </div>
  );
}

export default App;
```

Save the file and see the changes automatically reflected in your browser. This is the power of **hot reloading** provided by Vite.

---

### 5. Components in React

Components are the building blocks of a React application. They define the structure, logic, and appearance of the user interface. React allows you to create components using both **class-based** and **functional** approaches. Below, we cover the essentials of components in React, including props, event handling, and styling options.

**Props (short for properties)**

Props are how data is passed from parent components to child components. They allow components to be dynamic and reusable by accepting input data. For example:

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Greeting name="John" />;
}
```

In the above example, the `Greeting` component receives a prop called `name` and renders it within the `<h1>` tag. The value for `name` is passed from the parent component (`App`).

Props are **read-only**, meaning they cannot be modified by the child component. They are passed down from the parent and are used for customization.

**Class Components**  

Class components were the traditional way to define components before React introduced hooks. They extend from `React.Component` and have lifecycle methods. Example:

```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

class App extends React.Component {
  render() {
    return <Greeting name="John" />;
  }
}
```

**Functional Components**  

Functional components are now the preferred method for creating components, especially with the introduction of **hooks**. They are simpler and more concise than class components. Example:

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Greeting name="John" />;
}
```

Functional components are easier to work with and often result in cleaner code, especially with the use of hooks like `useState` and `useEffect`.

**Interpolation**

Interpolation is a way to embed variables or expressions inside JSX. You can use curly braces `{}` to interpolate JavaScript expressions inside the JSX. For example:

```jsx
function Greeting(props) {
  const greeting = "Hello";
  return <h1>{greeting}, {props.name}!</h1>;
}
```

Here, `greeting` and `props.name` are embedded within the JSX.

**Event Handling**

In React, events such as clicks, form submissions, and input changes are handled with **event handlers**. The syntax is similar to regular JavaScript, but React uses a **camelCase** naming convention for event names. Example of a click event:

```jsx
function Button() {
  const handleClick = () => {
    alert("Button clicked!");
  };

  return <button onClick={handleClick}>Click me</button>;
}
```

Here, `onClick` is a React event handler that is triggered when the button is clicked. The event handler `handleClick` is defined as a function that displays an alert when called.

---

### 6. Styling Components: Valid Options and Examples

React components can be styled in several ways, depending on your preferences and the needs of the project. Below are some common styling approaches:

**1. Traditional .css Files**  

We can use regular `.css` files to style React components. This is the traditional way of adding styles, and the styles are global unless scoped with class names. Example:

```css
/* styles.css */
.button {
  background-color: blue;
  color: white;
}
```

```jsx
import './styles.css';

function Button() {
  return <button className="button">Click me</button>;
}
```

**2. Sass**  

Sass is a popular CSS preprocessor that extends CSS with variables, nesting, and other features. React supports Sass out of the box with tools like Vite or Webpack. Example:

```scss
/* styles.scss */
$button-color: blue;

.button {
  background-color: $button-color;
  color: white;
}
```

```jsx
import './styles.scss';

function Button() {
  return <button className="button">Click me</button>;
}
```

**3. CSS Modules**  

CSS Modules are a way to scope your CSS to individual components. This prevents class name conflicts across components. Example:

```css
/* Button.module.css */
.button {
  background-color: blue;
  color: white;
}
```

```jsx
// Button.jsx
import styles from './Button.module.css';

function Button() {
  return <button className={styles.button}>Click me</button>;
}
```

**4. Styled Components**  

Styled Components is a popular library that lets you write CSS directly within JavaScript. It uses tagged template literals to define styles. Example:

```jsx
import styled from 'styled-components';

const Button = styled.button`
  background-color: blue;
  color: white;
`;

function App() {
  return <Button>Click me</Button>;
}
```

**5. JSS (JavaScript Style Sheets)**  

JSS is another approach to write CSS directly in JavaScript. It allows for dynamic styling based on props or state. Example:

```jsx
import { createUseStyles } from 'react-jss';

const useStyles = createUseStyles({
  button: {
    backgroundColor: 'blue',
    color: 'white',
  },
});

function Button() {
  const classes = useStyles();
  return <button className={classes.button}>Click me</button>;
}
```

---

### 7. Styling Components with Tailwind CSS

**Tailwind CSS** is a utility-first CSS framework that provides a collection of pre-defined classes you can apply directly in your JSX to style elements. This approach has gained significant popularity, especially in modern React applications, due to its efficiency, simplicity, and flexibility. Tailwind simplifies the CSS writing process and streamlines the development workflow, which is why it has become widely adopted.

**Advantages of Tailwind CSS:**

1. **Efficiency**: Tailwind allows you to apply styles directly in your JSX through utility classes. This reduces the need to switch between HTML and CSS files and eliminates the need to write custom CSS for many common design patterns. With utility classes, you can quickly style elements and make layout adjustments on the fly.

2. **Consistency**: By using predefined utility classes, you can ensure a consistent design system across your application. Tailwind provides a set of design utilities (e.g., `bg-blue-500`, `text-white`, `p-2`, `rounded`) that make it easier to maintain visual consistency throughout the project.

3. **No CSS Specificity Issues**: Traditional CSS often leads to problems with specificity when styling components. Since Tailwind uses atomic classes with predefined styles, you don’t have to worry about overriding styles or dealing with CSS specificity conflicts.

4. **Highly Customizable**: While Tailwind comes with a default set of utility classes, it is highly customizable. You can extend or modify the default theme using the `tailwind.config.js` file, allowing you to define custom colors, spacing, and more, making it flexible for any project.

5. **Responsive Design**: Tailwind comes with built-in responsive design utilities. You can add classes like `sm:`, `md:`, and `lg:` to style elements differently on various screen sizes. This makes it easy to create a fully responsive layout without writing custom media queries.

**Setting Up Tailwind in a React Project with Vite:**

To get started with Tailwind in your React project using Vite, follow these steps:

1. **Install Tailwind via npm**:
   
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

This installs the necessary dependencies and creates a default configuration file for Tailwind (`tailwind.config.js`).

2. **Set up PostCSS**

Create a `postcss.config.js` file in your project root that looks like this:

```javascript
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

__Note__: Vite uses PostCSS to process your CSS. Tailwind's as plugin will look for @tailwind directives in your CSS and generates the necessary utility classes. Autoprefixer automatically adds vendor-specific prefixes for better browser compatibility. Vite handles this by applying these plugins during both development and build stages, efficiently processing and bundling the resulting CSS into your final app.

3. **Set up Tailwind in your CSS entry point file (`src/index.css`)**:
   
```css
/* src/index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

These `@tailwind` directives pull in the base styles, components, and utility classes that are provided by Tailwind.

4. **Configure `tailwind.config.js`**:
   
```js
// tailwind.config.js
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

This configuration ensures that Tailwind processes all your JSX, JavaScript, TypeScript, and HTML files for classes used in your components.

5. **Using Tailwind in Your Components**:

Let’s walk through creating a button component with Tailwind. To keep things organized, we’ll start by structuring the project into separate folders. Specifically, we’ll create a folder for our components and then add a file for the button component.

```
/src
  /components
    Button.jsx
```

To define the button component in `Button.jsx`, we can do something like this:

```jsx
function Button() {
    return (
      <button className="bg-blue-500 text-white py-2 px-4 font-bold hover:bg-blue-600 transition-colors duration-200 ease-in-out">
        Click me
      </button>
    );
  }
  
  export default Button;
```

In this example:

- **`bg-blue-500`**: Sets the initial background color of the button to a blue shade.
- **`text-white`**: Makes the text color white.
- **`py-2 px-4`**: Adds padding to the button: `py-2` for vertical padding and `px-4` for horizontal padding.
- **`font-bold`**: Makes the text bold.
- **`hover:bg-blue-600`**: Changes the background color to a slightly darker blue when the button is hovered over.
- **`transition-colors`**: Smoothly transitions the background color on hover.
- **`duration-200`**: Sets the transition duration to 200 milliseconds.
- **`ease-in-out`**: Applies an easing effect for a smoother transition, both at the beginning and end.

Next, in the `App.jsx` file, import and use the `Button` component you just created.

```jsx
import './index.css'; // Imports the styling entry point enabling Tailwind across the application.
import Button from './components/Button'; // Importing the Button component

function App() {
  return (
    <div className="App p-10">
      <Button />
    </div>
  );
}

export default App;
```

The result will be:

![Button Component](print/button.png)

---

### 8. Local State and the `useState` hook

In React, **local/component state** refers to data that is specific to a component and controls how that component behaves or appears. This state is managed within the component itself and can be changed over time in response to user interactions, API responses, or other events. React provides the `useState` hook to manage this local state in functional components. The `useState` hook is used to define and update local state within a component. It takes an initial state as an argument and returns an array with two elements:

1. **State variable**: The current value of the state.
2. **State setter function**: A function that updates the state.

Sintax:

```js
const [state, setState] = useState(initialState);
```

- `state`: The current value of the state.
- `setState`: The function to update the state.
- `initialState`: The value that the state should have initially (can be any data type, such as a number, string, array, or object).

**Example 1: Basic Usage**

In this example, we create a counter that increments every time the button is clicked.

```jsx
import { useState } from 'react';

function Counter() {
  // Declare a state variable 'count' initialized to 0
  const [count, setCount] = useState(0);

  // Function to increment the count
  const increment = () => {
    setCount(count + 1); // Update the state by adding 1 to the current count
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default Counter;
```

- **`useState(0)`**: Initializes the `count` state variable with the value `0`.
- **`setCount(count + 1)`**: Updates the `count` state when the button is clicked, triggering a re-render of the component with the new state value.

**Example 2: Using State with Other Data Types (String)**

You can also use `useState` to manage other types of data, such as strings.

```jsx
import { useState } from 'react';

function Greeting() {
  const [name, setName] = useState('John');

  const changeName = () => {
    setName('Jane'); // Update state with a new name
  };

  return (
    <div>
      <p>Hello, {name}!</p>
      <button onClick={changeName}>Change Name</button>
    </div>
  );
}

export default Greeting;
```

In this case:
- **`useState('John')`** initializes the `name` state with the string `"John"`.
- **`setName('Jane')`** updates the `name` state when the button is clicked, causing the component to re-render with the new name.

**Example 3: Using State with Objects**

React state can hold complex data types, such as objects. When dealing with objects, we need to spread the previous state to avoid overwriting existing properties.

```jsx
import { useState } from 'react';

function UserProfile() {
  const [user, setUser] = useState({ name: 'John', age: 30 });

  const updateAge = () => {
    setUser(prevState => ({
      ...prevState, // Spread the previous state
      age: prevState.age + 1, // Update the age property
    }));
  };

  return (
    <div>
      <p>Name: {user.name}</p>
      <p>Age: {user.age}</p>
      <button onClick={updateAge}>Increase Age</button>
    </div>
  );
}

export default UserProfile;
```

In this example:
- **`useState({ name: 'John', age: 30 })`** initializes the state with an object.
- **`setUser(prevState => ({ ...prevState, age: prevState.age + 1 }))`** updates the `age` property of the `user` object without losing the `name` property.

---

### 9. Side Effects

In React, **side effects** refer to any operations or actions that interact with the outside world, such as fetching data from an API, updating the DOM directly, setting up subscriptions, or timers. These actions are not directly related to the component's render process, but they can affect the component's behavior. React provides the `useEffect` hook to handle side effects efficiently.

The `useEffect` hook runs after the component renders and can be used to trigger things like data fetching, subscriptions, or directly manipulating the DOM. It accepts two arguments: a function that contains the side effect logic and an optional dependency array.

```jsx
import { useEffect, useState } from 'react';

function ExampleComponent() {
  const [data, setData] = useState(null);

  // Side effect to fetch data
  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(result => setData(result))
      .catch(error => console.log('Error fetching data', error));
  }, []); // Empty array means the effect runs only once after the initial render

  return <div>{data ? data : 'Loading...'}</div>;
}
```

**Dependency Arrays and Controlling Re-renders**

The **dependency array** controls when the effect should run. If the array is empty (`[]`), the effect will only run once when the component mounts. If we pass specific state or props in the dependency array, the effect will only run when those values change.

So we can have situations like this:

```jsx
useEffect(() => {
  console.log('Effect ran on mount');
}, []); // This will only run the effect once, when the component first renders.
```

Or like this:

```jsx
useEffect(() => {
  console.log('Effect ran because count or name changed:', count, name);
}, [count, name]); // Runs when either 'count' or 'name' changes
```

If we include multiple dependencies in the array, the effect will run whenever any of the values in the array change.

**Fetching data with async/await**

Fetching data is one of the most common side effects in React. The `useEffect` hook is ideal for triggering an API call when a component mounts, and we can use the `async/await` syntax for handling asynchronous operations more cleanly. Here’s an example closer to what a real-world React application might do:

```jsx
import { useState, useEffect } from 'react';

function FetchDataExample() {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch('https://api.example.com/items');
        const result = await response.json();
        setData(result);
      } catch (error) {
        console.error('Error fetching data:', error);
      } finally {
        setLoading(false);
      }
    };
    fetchData();
  }, []); // Empty dependency array means it runs once on mount

  return (
    <div>
      {loading ? <p>Loading...</p> : <ul>{data.map(item => <li key={item.id}>{item.name}</li>)}</ul>}
    </div>
  );
}
```

In this example, `useEffect` calls the `fetchData` function when the component mounts. The `loading` state helps to display a loading message while the data is being fetched.

---

### 10. Understanding Lifecycle in React

In React, understanding the **lifecycle** of components is crucial as it defines how and when code is executed during the component's existence. The component lifecycle differs between **class components** and **functional components** due to syntax, performance optimizations, and features like hooks. The main React's **lifecycle states** are:

- **Mounting**: In **class components**, `componentDidMount` runs after the first render. In **functional components**, use `useEffect` with `[]`.  
- **Updating**: Triggered by state/prop changes. Class components use `componentDidUpdate`, while functional components use `useEffect` with dependencies.  
- **Unmounting**: Class components use `componentWillUnmount`, while functional components rely on a cleanup function in `useEffect`.  

NOTE: Deprecated methods like `componentWillMount` and `componentWillUpdate` should be avoided.

Within an application, our implementations could be as such:

**1. Class components**

With class components, we use named lifecycle methods for the specific stage we want to capture:

```jsx
import React, { Component } from "react";

class Example extends Component {
  componentDidMount() {
    console.log("Component mounted: Perform side effects here!");
  }

  componentDidUpdate() {
    console.log("Component updated: Respond to prop or state changes!");
  }

  componentWillUnmount() {
    console.log("Component will unmount: Cleanup here!");
  }

  render() {
    return <div>Hello, Class Component!</div>;
  }
}
```

**2. Functional components**

Functional components can achieve the same behavior as class components using the `useEffect` hook. The lifecycle methods in class components map to specific usages of `useEffect`:

   - `componentDidMount` → **useEffect** with an empty dependency array.  
   - `componentDidUpdate` → **useEffect** with dependencies specified.  
   - `componentWillUnmount` → **Cleanup function** inside `useEffect`.

When discussing the lifecycle of functional components, it's important to also consider the **cleanup function**. In React, a cleanup function is an optional yet essential feature within the `useEffect` hook. React calls this function before the component unmounts or when the dependencies of the effect change, preventing memory leaks and ensuring proper resource management. Cleanup is useful for canceling timers, aborting API requests, or unsubscribing from event listeners. Without it, lingering side effects can lead to unintended behavior. React executes the cleanup function before re-running the effect or removing the component from the DOM, maintaining optimal performance and stability. Practical Example:  
  
```jsx
   import React, { useState, useEffect } from "react";

   function TimerComponent() {
     const [seconds, setSeconds] = useState(0);

     useEffect(() => {
       const timer = setInterval(() => {
         setSeconds((prev) => prev + 1);
       }, 1000);

       // Cleanup function: clear the interval when unmounting
       return () => {
         clearInterval(timer);
         console.log("Timer cleaned up");
       };
     }, []); // Runs only on mount

     return <div>Seconds passed: {seconds}</div>;
   }
```

In this case, we can encapsulate the concept of the lifecycle within functional components like this:

```jsx
useEffect(() => {
  // Runs once on mount
}, []); // empty dependency array

useEffect(() => {
  // Runs on mount + whenever `dependency` changes
}, [dependency]); // specify a single dependency

useEffect(() => {
  // Runs on mount + when `dep1` OR `dep2` change
}, [dep1, dep2]); // multiple dependencies

useEffect(() => {
  // Runs on every render (mount and update)
}); // no dependency array

useEffect(() => {
  // Runs on mount, when `dependency` changes, and cleanup runs on unmount
  return () => {
    // Cleanup logic here
  };
}, [dependency]); // cleanup tied to dependency changes or unmount
```

---

### 11. Essential React Concepts: Destructuring, Keys, Props Drilling, and Lifting State

**1. Destructuring**

Destructuring simplifies the process of extracting properties from objects or arrays, making your code cleaner and more readable. In React, it is commonly used to access props or state. Example:

```jsx
function UserCard({ name, age }) {
  return (
    <div>
      <h2>{name}</h2>
      <p>Age: {age}</p>
    </div>
  );
}
```

This is equivalent to:  
```jsx
function UserCard(props) {
  const { name, age } = props;
  return (
    <div>
      <h2>{name}</h2>
      <p>Age: {age}</p>
    </div>
  );
}
```

Benefits:  

- Reduces repetitive `props.propertyName`.  
- Makes the code concise and focused.

---

**2. Single Key for Lists**

When rendering lists in React, each element must have a unique `key` prop. Keys help React efficiently identify changes, additions, and removals in a list. They enable React to update the DOM efficiently and prevent unintended behavior by maintaining component identity. Example:

```jsx
function ItemList({ items }) {
  return (
    <ul>
      {items.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}
```

Ps. Avoid using indices as keys, as this can lead to bugs when items are reordered or removed.

**3. Props Drilling**

Props drilling occurs when data is passed through multiple layers of components, even when only the deepest child uses the data. This is common in React apps but can lead to unnecessary complexity. Example:

```jsx
function Grandparent() {
  const message = "Hello, React!";
  return <Parent message={message} />;
}

function Parent({ message }) {
  return <Child message={message} />;
}

function Child({ message }) {
  return <div>{message}</div>;
}
```

Issues with Props Drilling:

- Increases coupling between components.  
- Makes components harder to maintain.

**4. Lifting State Up Between Components**

In React, shared state should reside in the closest common ancestor of the components that need it. This practice, called **lifting state up**, prevents duplication and ensures consistent data. Example:

```jsx
import React, { useState } from "react";

function Parent() {
  const [count, setCount] = useState(0);

  const onAdd = () => setCount(count + 1);

  return (
    <div>
      <Child count={count} onIncrement={onAdd} />
    </div>
  );
}

function Child({ count, onIncrement }) {
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={onIncrement}>Increment</button>
    </div>
  );
}
```

In this example:  

- The `Parent` component manages the state (`count`).  
- The `Child` component displays and updates the state using props (`count` and `onIncrement`).

Benefits of Lifting State:  

- Eliminates redundant state.  
- Ensures a single source of truth.

---

### 12. Components: Composition, Presentation and Best Practices

React development is all about creating modular, reusable, and maintainable components. By following React's philosophy of **composition over inheritance**, developers can design flexible and scalable applications.

**1. Composition Over Inheritance**

React prioritizes **composition** as the main way to build UIs. Instead of creating deep inheritance hierarchies, React encourages combining small, focused components to achieve desired functionality. The benefits of this approach are:

A) Simplicity:

   - Composition enables clear and modular designs by allowing components to be combined like building blocks.  
   - Inheritance introduces unnecessary complexity with tightly coupled relationships between parent and child components.

B) Flexibility:

   - Composition allows components to adapt to various use cases without needing to modify or extend their structure.  
   - You can combine and reuse components in different contexts through props and children.

C) Encapsulation:

   - Components in React interact only through well-defined interfaces (props), ensuring that behavior is self-contained and predictable.  

**2. Types of Components: Presentation vs. Domain Components**

**1. Presentation Components (or "Dumb" Components)**  

These focus on **how things look** and rely on props for data and actions. They do not manage state or interact with APIs. Example: 

```jsx
// Button.jsx
import React from "react";

const Button = ({ label, onClick }) => (
  <button onClick={onClick}>
    {label}
  </button>
);

export default Button;
```

Key Features of Presentation Components:

- **Stateless**: They do not manage their own state.  
- **Reusable**: Focus solely on rendering the UI and depend on props for behavior.  

**2. Domain Components (or "Smart" Components)**  

These handle **how things work** by managing state, handling business logic, and coordinating between different presentation components. Example:

```jsx
// Counter.jsx
import React, { useState } from "react";
import Button from "./Button";

const Counter = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>Count: {count}</h1>
      <Button label="Increase" onClick={() => setCount(count + 1)} />
      <Button label="Decrease" onClick={() => setCount(count - 1)} />
    </div>
  );
};

export default Counter;
```

Key Features of Domain Components:

- Manage **state** and **business logic**.  
- Combine multiple presentation components to deliver functionality.

**3. Best Practices for Creating React Components**

A) Keep Components Small and Focused

- Single Responsibility Principle: Each component should do one thing well.  
- Break large components into smaller ones to improve readability and maintainability.

Example:

```jsx
// Header.jsx
import React from "react";
import Logo from "./Logo";
import Navigation from "./Navigation";

const Header = () => (
  <header>
    <Logo />
    <Navigation />
  </header>
);

export default Header;
```

By delegating responsibilities to `Logo` and `Navigation`, `Header` remains clean and focused.

B) Leverage Composition Using `children`

The `children` prop enables the injection of other components or content. This makes them highly reusable and composable. 

Example:

```jsx
// Layout.jsx
import React from "react";

const Layout = ({ children }) => (
  <div>
    {children}
  </div>
);

export default Layout;
```

Usage:

```jsx
import Layout from "./Layout";

const App = () => (
  <Layout>
    <h1>Welcome</h1>
    <p>This is the main content inside the layout.</p>
  </Layout>
);
```

C) Avoid Overusing State

- Place state in the component where it is most relevant.  
- Avoid passing excessive state or logic down multiple levels of components (prop drilling). Instead, use React Context or state management libraries when needed.

**4. Applying Composition in Practice**

The example below follows the principles of composition, keeping each component focused on a specific responsibility:

```jsx
// TodoItem.jsx
import React from "react";

const TodoItem = ({ todo }) => {
  return <li>{todo}</li>;
};

export default TodoItem;
```

```jsx
// TodoList.jsx
import React from "react";
import TodoItem from "./TodoItem";

const TodoList = ({ todos }) => {
  return (
    <ul>
      {todos.map((todo, index) => (
        <TodoItem key={index} todo={todo} />
      ))}
    </ul>
  );
};

export default TodoList;
```

```jsx
// AddTodo.jsx
import React, { useState } from "react";

const AddTodo = ({ addTodo }) => {
  const [inputValue, setInputValue] = useState("");

  const handleAddTodo = () => {
    if (inputValue.trim()) {
      addTodo(inputValue);
      setInputValue(""); 
    }
  };

  return (
    <div>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
        placeholder="Add a new todo"
      />
      <button onClick={handleAddTodo}>Add</button>
    </div>
  );
};

export default AddTodo;
```

### Key Points:

1. **App.jsx**: Manages the state (`todos`) and passes data/handlers to child components via props.
2. **TodoList.jsx**: Renders the list of todos by iterating through the `todos` array and passing each item to **TodoItem**.
3. **TodoItem.jsx**: Displays an individual todo item.
4. **AddTodo.jsx**: Handles user input for adding new todos and communicates the new item back to the parent via `addTodo`.

This structure promotes separation of concerns, making the codebase easier to understand, maintain, and scale.

---

### 13. Higher-Order Components (HOCs)

In React, a **Higher-Order Component (HOC)** is an advanced technique for reusing component logic. An HOC is a function that takes a component as an argument and returns a new component with enhanced behavior or additional props. HOCs are not a feature of React itself but a pattern that leverages React's compositional nature. They are commonly used to:

- Share functionality between components.
- Abstract repetitive logic (e.g., handling authentication, logging, or state management).
- Modify or enhance components without altering their original implementation.

Signature of an HOC:  

```jsx
const EnhancedComponent = higherOrderComponent(WrappedComponent);
```

A HOC wraps a component and returns a new one, injecting additional props or logic. Here's a basic example:

```jsx
import React from "react";

// Higher-Order Component
function withUserName(WrappedComponent) {
  return function EnhancedComponent(props) {
    return <WrappedComponent {...props} name="John Doe" />;
  };
}

// Regular Component
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}

// Enhanced Component
const GreetingWithUserName = withUserName(Greeting);

function App() {
  return <GreetingWithUserName />;
}
```

Above we have:

- The `withUserName` HOC adds the `name` prop to the `Greeting` component.
- The enhanced component (`GreetingWithUserName`) renders with the added prop.

**Key Use Cases for HOCs**

1. **Code Reusability**: Share logic across multiple components.
2. **Conditional Rendering**: Implement access control (e.g., authentication).
3. **Data Fetching**: Abstract API requests and inject data into wrapped components.

**Practical example 1: Conditional Rendering with HOC**

The idea here is to determine whether to render the original component or something else, based on a condition. Example:

```jsx
import React from "react";

// HOC for authentication
function withAuth(WrappedComponent) {
  return function AuthenticatedComponent(props) {
    const isAuthenticated = true; // Replace with real auth logic
    if (!isAuthenticated) {
      return <h2>Please log in to access this content.</h2>;
    }
    return <WrappedComponent {...props} />;
  };
}

// Regular Component
function Dashboard() {
  return <h1>Welcome to the Dashboard!</h1>;
}

// Enhanced Component
const ProtectedDashboard = withAuth(Dashboard);

function App() {
  return <ProtectedDashboard />;
}
```

In the code above, the `withAuth` HOC verifies authentication before rendering the `Dashboard` component. If the user is not authenticated, it displays a fallback message.

**Practical example 2: Data Fetching with HOC**

The idea here is to use a Higher-Order Component to manage data fetching. Example:

```jsx
import React, { useState, useEffect } from "react";

// HOC for data fetching
function withDataFetching(WrappedComponent, apiUrl) {
  return function DataFetchingComponent(props) {
    const [data, setData] = useState(null);
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState(null);

    useEffect(() => {
      const fetchData = async () => {
        try {
          const response = await fetch(apiUrl);
          if (!response.ok) {
            throw new Error("Network response was not ok");
          }
          const data = await response.json();
          setData(data);
        } catch (error) {
          setError(error.message);
        } finally {
          setLoading(false);
        }
      };

      fetchData();
    }, [apiUrl]);

    if (loading) {
      return <p>Loading...</p>;
    }

    if (error) {
      return <p>Error: {error}</p>;
    }

    return <WrappedComponent {...props} data={data} />;
  };
}

// Regular Component
function UserList({ data }) {
  return (
    <ul>
      {data.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}

// Enhanced Component
const UserListWithData = withDataFetching(UserList, "https://jsonplaceholder.typicode.com/users");

function App() {
  return <UserListWithData />;
}
```

Here, the `withDataFetching` HOC retrieves data from an API and passes it as a prop to the `UserList` component. The original component stays focused on rendering, while the HOC handles the data fetching.

**Best Practices for Using HOCs**

- **Avoid Overwrapping**: Nesting too many HOCs can lead to "wrapper hell", making debugging difficult.
- **Pass Props Transparently**: Always forward props to the wrapped component using `{...props}` to ensure it remains flexible.
- **Name Your HOCs Clearly**: Use descriptive names like `withAuth`, `withLogging`, or `withDataFetching`.

**Caveats of HOCs**

- **Can Be Overused**: Modern alternatives like React **Hooks** or the **Context API** can sometimes replace HOCs.
- **Static Methods Are Not Copied**: When wrapping a component, static methods (e.g., `WrappedComponent.someStaticMethod`) are not transferred to the enhanced component. Use libraries like `hoist-non-react-statics` to copy them.










