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

### 6. Styling React Components: Valid Options and Examples

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

### 7. Styling React Components: Using Tailwind CSS

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

