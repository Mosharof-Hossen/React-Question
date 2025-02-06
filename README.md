## React Core

### **1. What is React? (React কী?)**

React is a **JavaScript library** used for building user interfaces. It follows a **component-based architecture** and optimizes performance using the **virtual DOM**.

*React হলো একটি **JavaScript লাইব্রেরি**, যা **UI** তৈরি করার জন্য ব্যবহৃত হয়। এটি **component-based architecture** অনুসরণ করে এবং **virtual DOM** ব্যবহার করে পারফরম্যান্স অপটিমাইজ করে।*

### **2. What is the Virtual DOM? (Virtual DOM কী?)**

The Virtual DOM is a **lightweight copy** of the actual DOM that React uses to **efficiently update the UI**.
When you make changes in React, React first updates the **Virtual DOM** and then updates only the necessary changes to the **actual DOM**, making the app faster.

🔹 Why Virtual DOM is Important? (Virtual DOM কেন গুরুত্বপূর্ণ?)

1️⃣ **Speed** → Directly updating the **actual DOM** can be slow. By using the **Virtual DOM**, React makes updates more efficiently, improving speed.
2️⃣ **Efficiency** → Instead of updating the whole page, React compares the old **Virtual DOM** with the new one and updates only the parts that have changed.

🔹 How React Uses Virtual DOM? (React কীভাবে Virtual DOM ব্যবহার করে?)

1️⃣ **Step 1: React creates a Virtual DOM**

(React first creates the **Virtual DOM**, which is a virtual copy of the **actual DOM**.)

2️⃣ **Step 2: React updates Virtual DOM**

(When a **state** or **prop** changes, React makes those changes in the **Virtual DOM** first.)

3️⃣ **Step 3: React compares Virtual DOM with actual DOM**

(React compares the old **Virtual DOM** with the new **Virtual DOM**.)

4️⃣ **Step 4: React updates the actual DOM efficiently**

React কেবলমাত্র সেই অংশগুলো আপডেট করে যা পরিবর্তিত হয়েছে, এবং এতে **actual DOM**-এ অল্প পরিবর্তন আসে, যা অ্যাপকে দ্রুত কাজ করতে সাহায্য করে।

(React updates only the parts that have changed, resulting in minimal changes to the **actual DOM**, which helps the app perform faster.)

🔹 Why Use Virtual DOM? (Virtual DOM কেন ব্যবহার করা উচিত?)

- Faster Updates
- Less Re-rendering
- Better Performance

### 3. React-এর Reconciliation প্রক্রিয়া ব্যাখ্যা করুন।

Reconciliation is the process where React updates the UI using the Virtual DOM. When  change a state or props, React compares the old and new Virtual DOM and updates only the changed parts in the actual DOM, making the app faster and more efficient.

### **4. What are the key features of React? (React-এর মূল বৈশিষ্ট্য কী কী?)**

- JSX (JavaScript XML) - JSX (JavaScript XML) is a syntax extension of JavaScript that allows us to write HTML-like code inside JavaScript.
- Component-Based Architecture
- Virtual DOM
- Unidirectional Data Flow
- React Hooks
- Client-side Rendering (Next.js-এর মাধ্যমে)

### **5. How many types of components are there in React? (React-এর কত ধরনের কম্পোনেন্ট আছে?)**

- **Class Component**
- **Functional Component** (Recommended in modern React)

### **6. What is the difference between a class component and a functional component?**

| Feature | Class Component | Functional Component |
| --- | --- | --- |
| Syntax | Uses `class` keyword | Uses simple functions |
| State | Uses `this.state` | Uses `useState` hook |
| Performance | Less optimized | More optimized |
| Hooks Support | No | Yes |

### 7. What is Context API? (Context API কী?)

Context API allows **global state management** without prop drilling.

Context API is a built-in feature in React used to avoid props drilling. If a piece of data or state needs to be shared across multiple child components, then Context API should be used because it reduces the complexity of prop drilling.

### 8. State এবং Props-এর মধ্যে পার্থক্য কী?

✅ **State** → **Component-এর নিজের ডাটা**, যা পরিবর্তন (update) হতে পারে।
(**State is the component’s own data that can be changed.**)

✅ **Props →** Props are data passed from a parent component to a child component and cannot be modified by the child.

## Hooks And State

### 1. What is State in React? (React-এ State কী?)

**State** is an **object** that stores data that can change over time. When the **state changes, the component automatically re-renders**, and the UI updates.

### 2. What are props in React? (React-এ props কী?)

Props (short for "Properties") are **read-only data** passed from **parent to child components**.

### 3. React Hooks (React Hooks কী?)

React Hooks are special functions that allow you to use **state and lifecycle features** inside a **React functional component** without using a **class component**.

🔹 Why Use Hooks? (Hooks কেন ব্যবহার করব?)

আগে React Class Component-এ state এবং lifecycle method (যেমন componentDidMount, componentDidUpdate) ব্যবহার করতে হতো। কিন্তু Hooks আসার পর এগুলো Functional Component-এর মধ্যেই করা যায়, যা কোডকে clean, short এবং সহজ করে তোলে। 

(Before Hooks, React Class Components were required to use state and lifecycle methods (like componentDidMount, componentDidUpdate). But with Hooks, we can now do these inside a Functional Component, making the code clean, short, and simple.)

### 4. What is useEffect in React? (React-এ useEffect কী?)

`useEffect` is a hook used for handling **side effects** in React components (e.g., API calls, subscriptions).

| **useEffect() (ইউজএফেক্ট)** | **useLayoutEffect() (ইউজলেআউটএফেক্ট)** |
| --- | --- |
| **useEffect()** runs asynchronously after the component renders, meaning it does not block the UI | useLayoutEffect() runs synchronously after the component renders but before the UI update, which may block rendering. |
| useEffect() is good for API calls, event listeners, data fetching, and subscriptions because it runs in the background. | useLayoutEffect() is useful for DOM manipulation, layout measurements, and animations because it executes before the browser paints the screen. |

### 5. useReducer() এবং useState() এর মধ্যে কোনটি কখন ব্যবহার করবেন?

| useState() | useReducer() |
| --- | --- |
| useState() is best for simple state management, where the state is a single value or a few values. | useReducer() is best for complex state logic, where the state depends on multiple actions or updates. |
| useState() is easier to use |  |
|  |  |

### 6. Redux ? ,এর সুবিধাগুলো কী?

✅ **Redux** is a state management library that helps manage and centralize the state of JavaScript applications. It can be used with frameworks like **React**, **Angular**, or any other JavaScript framework.

Redux-এর সুবিধাগুলো (Advantages of Redux):

- Centralized State Management
- **Redux** makes state changes predictable
- Debugging Support:  With **Redux DevTools**, developers can track state changes and analyze how the app is functioning.
- Ease of Maintenance
- Middleware Support: **Redux** supports **middleware** like **redux-thunk.**

## Performance Optimization:

### How to optimize performance in React? (React-এর পারফরম্যান্স কীভাবে অপটিমাইজ করা যায়?)

- **Using React.memo** (Prevents unnecessary re-renders)
- **Using useCallback & useMemo** (Optimizes function and value references)
- **Efficiently updating the state**
- **Avoiding unnecessary re-renders with key props**

### Client-Side Rendering (CSR) এবং Server-Side Rendering (SSR)-এর পার্থক্য

| **Aspect** | **Client-Side Rendering (CSR)** | **Server-Side Rendering (SSR)** |
| --- | --- | --- |
| **How it works** | The browser loads a minimal HTML file, then fetches JavaScript, which dynamically updates the UI using data from API calls. | The server generates the HTML content with data, and sends it to the browser, which displays the complete page immediately. |
| **Initial Load Time** | Initial load can be slow as JavaScript and data need to load before rendering. | Faster initial load as the full HTML page is delivered to the browser. |
| **SEO Performance** | SEO can be less effective as search engines might have difficulty indexing content that is rendered client-side. | SSR provides better SEO performance since the content is already rendered when the page is loaded. |
| **Use Case** | Ideal for Single Page Applications (SPA) where content is updated dynamically. | Suitable for static websites or applications that require faster initial page loads, such as blogs, news sites, or e-commerce pages. |
