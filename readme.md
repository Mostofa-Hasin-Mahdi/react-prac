## 📹 Notes for all the stuff I've learned about React JS

### 🚀 React Project Creation with `create-react-app`

```bash
npx create-react-app 01basicreact
```

- **npx**: Node Package Runner — allows you to run packages without installing them globally.  
- **create-react-app**: A utility to scaffold a new React project.  
- **01basicreact**: The name of your React project.

---

📁 **Understanding React Project Structure**  
🗂 **package.json** (Main Entry Point)  
Contains metadata about the project.

Lists:

- 📦 Project name  
- 🔗 Dependencies  
- 🧪 Testing libraries  
- 🛠 Scripts  
- 📈 **web-vitals**  
  Used to measure and report app performance (Core Web Vitals like load time, responsiveness, etc.).

📜 **Scripts in package.json**

| Script | Purpose |
|--------|---------|
| `start` | Runs the project in development mode. |
| `build` | Creates a production-ready build (compiled, optimized). |
| `test`  | Runs test cases. |
| `eject` | Ejects from default CRA settings to gain full control of configurations. |

---

⚡ **Creating a Project with Vite**

```bash
npm create vite@latest
```

Prompts for:

- 📛 Project name  
- 🧱 Framework and variant (e.g., React + JS/TS)

**Steps After Creation:**

1. Navigate into the project folder.  
2. Install dependencies:  
   ```bash
   npm install
   ```
3. Run the development server:  
   ```bash
   npm run dev
   ```

---

### 🧠 Understanding the React Flow and Structure 

📦 **package-lock.json**  
Contains the exact versions of installed dependencies — locks dependencies to a specific version.

📁 **Main Work Folders**  
Most development is done inside:

- **src/** – Source files  
- **public/** – Static files

📄 **public/manifest.json**  
Contains metadata about how the app appears on mobile devices (e.g., icon, theme color).

📄 **public/robots.txt**  
Used to guide search engine crawlers about which parts of the site to index.

📄 **public/index.html**  
Acts as the **Single Page Application (SPA)** root. The base HTML file where React components are injected and DOM manipulation begins.

---

📄 **src/index.js**  
- `import React from 'react';` → Imports the React core library.  
- `import ReactDOM from 'react-dom/client';` → Imports React DOM methods for rendering in the browser.

🌳 **DOM vs Virtual DOM**  
- The **DOM** is a tree structure for HTML elements.  
- React creates a **Virtual DOM** — a lightweight copy of the DOM. It compares changes (diffing) and updates only what's necessary in the real DOM for performance.

🧬 **JSX**  
- Syntax that allows you to write HTML-like code inside JavaScript.  
- Enables rendering of UI components using familiar HTML tags.

💡 **Function-Based Components**  
React allows writing functions that return JSX. These are components that render parts of your UI.

📦 `"react-scripts": "5.0.1"`  
Used in Create React App (CRA) to run scripts and load HTML.

---

🌀 **Vite-Specific Notes**

📄 **main.jsx**  
Entry point for React apps created using Vite. It's referenced via a script tag in `index.html`, not injected by CRA tools.

📥 **Importing & Using Components**
1. **Export** the component in its file:
   ```js
   export default Meatbox;
   ```
2. **Import** it where needed:
   ```js
   import Meatbox from "./assets/eagle";
   ```
3. **Render** it:
   ```jsx
   <Meatbox />
   ```

🧩 **Rendering Multiple Components**  
Wrap them in **fragments** to avoid extra divs:
```jsx
<>
  <Component1 />
  <Component2 />
</>
```

📐 **Component Naming Rules (React/Vite)**

- Always start component function names with a **capital letter**.
  ```js
  function Meatbox() {
    // Component code
  }
  ```
- For **Vite**, use `.jsx` file extensions.  
- Optionally, capitalize the filename (e.g., `Meatbox.jsx`).
- 
---

🔧 **React Hooks and State Management**

🔄 **Why Use Hooks in React?**

In classic JavaScript, you could manipulate and show data directly using DOM methods like getElementById.
In React, while you can still manipulate data, it won’t automatically reflect in the UI unless you use hooks.

🧲 **What is a Hook?**

Hooks are special functions in React that let you “hook into” React features like state and lifecycle methods.

📦 **Importing Hooks**
Use this import to bring in a hook:
```jsx

import { useState } from 'react';
```
🧠 **useState Hook**

- Allows state management within function components.

- Updates the state variable and reflects changes on the UI (DOM).

- Syntax: 
```jsx

const [stateVariable, setStateFunction] = useState(defaultValue);
```
🔢 **Example:**
```jsx

let [counter, setCounter] = useState(15);
```
- counter → The state variable.

- setCounter() → The function to update the variable.

- Whenever setCounter() is called, the component re-renders with the new value.

⚠️ **Note:** The change here refers to DOM updates — not just changing the value in memory, but also updating what is rendered on the screen.
