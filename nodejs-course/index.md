### **Full Stack Web Development Course: Instructor Slide Content**

---

## **Week 1: Foundations of Web Development**

### **Module 1: Introduction to Web Development & Environment Setup**

---

#### **Slide 1: Title Slide**
- **Title:** Introduction to Web Development & Environment Setup
- **Subtitle:** Week 1, Module 1
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the role of a full stack developer
- **Learn** the basics of Node.js and its ecosystem
- **Set up** the development environment (Visual Studio Code, Git, Node.js)
- **Initialize** a Git repository and push to GitHub
- **Create** a simple "Hello World" Node.js application

---

#### **Slide 3: What is Full Stack Web Development?**
- **Definition:** Building both frontend (client-side) and backend (server-side) of web applications
- **Components:**
  - **Frontend:** User interface, user experience
  - **Backend:** Server logic, databases, APIs
- **Importance:** Enables comprehensive understanding and control over entire application

---

#### **Slide 4: Introduction to Node.js**
- **Definition:** A JavaScript runtime built on Chrome's V8 engine
- **Features:**
  - Asynchronous and event-driven
  - Non-blocking I/O operations
  - Suitable for scalable network applications
- **Use Cases:** Web servers, real-time applications, APIs

---

#### **Slide 5: The Node.js Ecosystem**
- **npm (Node Package Manager):**
  - Largest ecosystem of open source libraries
  - Manage project dependencies
- **Modules:** Reusable code components
- **Frameworks:** e.g., Express.js for building web applications

---

#### **Slide 6: Setting Up Visual Studio Code (VS Code)**
- **Download & Installation:**
  - Visit [Visual Studio Code](https://code.visualstudio.com/)
  - Choose the appropriate installer for your OS
- **Key Features:**
  - Intellisense (code completion)
  - Integrated terminal
  - Extensions for enhanced functionality

---

#### **Slide 7: Installing Git and Configuring GitHub**
- **Git Installation:**
  - Visit [Git Downloads](https://git-scm.com/downloads)
  - Install Git and verify installation via terminal (`git --version`)
- **Configuring Git:**
  - Set username: `git config --global user.name "Your Name"`
  - Set email: `git config --global user.email "you@example.com"`
- **GitHub Setup:**
  - Create a GitHub account if not already
  - Generate SSH keys for secure communication

---

#### **Slide 8: Introduction to npm (Node Package Manager)**
- **Purpose:** Manage project dependencies and scripts
- **Key Commands:**
  - `npm init` - Initialize a new Node.js project
  - `npm install` - Install dependencies
  - `npm update` - Update packages
- **package.json:** Manages project metadata and dependencies

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Install VS Code, Git, and Node.js
  2. Initialize a Git repository and push to GitHub
  3. Create and run a "Hello World" Node.js application

---

#### **Slide 10: Activity Step 1 - Installing Tools**
- **Instructions:**
  - **Visual Studio Code:**
    - Download from [VS Code](https://code.visualstudio.com/)
    - Install and launch
  - **Git:**
    - Download from [Git](https://git-scm.com/downloads)
    - Install and verify (`git --version`)
  - **Node.js:**
    - Download from [Node.js](https://nodejs.org/)
    - Install and verify (`node -v` and `npm -v`)

---

#### **Slide 11: Activity Step 2 - Initialize Git Repository**
- **Instructions:**
  1. Open VS Code and navigate to the terminal
  2. Create a new directory: `mkdir fintech-app && cd fintech-app`
  3. Initialize Git: `git init`
  4. Create a `.gitignore` file and add `node_modules/`
  5. Add and commit: `git add .` then `git commit -m "Initial commit"`
  6. Create a repository on GitHub
  7. Link local repo to GitHub: `git remote add origin <repository_url>`
  8. Push to GitHub: `git push -u origin main`

---

#### **Slide 12: Activity Step 3 - Create "Hello World" Application**
- **Instructions:**
  1. Initialize Node.js project: `npm init -y`
  2. Create `server.js` file with the following content:
     ```javascript
     const http = require('http');

     const hostname = '127.0.0.1';
     const port = 3000;

     const server = http.createServer((req, res) => {
       res.statusCode = 200;
       res.setHeader('Content-Type', 'text/plain');
       res.end('Hello World\n');
     });

     server.listen(port, hostname, () => {
       console.log(`Server running at http://${hostname}:${port}/`);
     });
     ```
  3. Run the application: `node server.js`
  4. Open browser and navigate to `http://127.0.0.1:3000/` to see "Hello World"

---

#### **Slide 13: Reviewing the Code**
- **Explanation:**
  - **http Module:** Built-in Node.js module for creating servers
  - **server.listen():** Starts the server on specified hostname and port
  - **Request Handler:** Sends "Hello World" response for any request
- **Live Demonstration:** Run the server and show output in browser

---

#### **Slide 14: Committing and Pushing Changes**
- **Instructions:**
  1. Stage changes: `git add server.js package.json`
  2. Commit changes: `git commit -m "Add Hello World server"`
  3. Push to GitHub: `git push`
- **Best Practices:**
  - Write descriptive commit messages
  - Commit frequently with logical changes

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Introduction to full stack development
  - Overview of Node.js and npm
  - Setting up development environment
  - Creating and deploying a simple Node.js application
- **Questions:** Open floor for any student queries

---

### **Module 2: JavaScript Fundamentals (ES6+)**

---

#### **Slide 1: Title Slide**
- **Title:** JavaScript Fundamentals (ES6+)
- **Subtitle:** Week 1, Module 2
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** ES6+ features and enhancements
- **Learn** about variables, data types, and structures
- **Master** functions, arrow functions, and asynchronous JavaScript
- **Apply** ES6 features in practical coding scenarios

---

#### **Slide 3: Variables in ES6**
- **let vs const vs var:**
  - **let:** Block-scoped, reassignable
  - **const:** Block-scoped, immutable binding
  - **var:** Function-scoped, hoisted (avoid using)
- **Examples:**
  ```javascript
  let age = 25;
  age = 26; // Valid

  const name = 'Alice';
  // name = 'Bob'; // Error

  var count = 10;
  ```

---

#### **Slide 4: Data Types and Structures**
- **Primitive Types:** String, Number, Boolean, Null, Undefined, Symbol
- **Reference Types:** Objects, Arrays, Functions
- **Examples:**
  ```javascript
  // Primitives
  let str = "Hello";
  let num = 100;
  let isActive = true;

  // Arrays
  let fruits = ['Apple', 'Banana', 'Cherry'];

  // Objects
  let user = {
    name: 'John Doe',
    age: 30,
    isAdmin: false
  };
  ```

---

#### **Slide 5: Functions and Arrow Functions**
- **Traditional Functions:**
  ```javascript
  function greet(name) {
    return `Hello, ${name}`;
  }
  ```
- **Arrow Functions:**
  ```javascript
  const greet = (name) => `Hello, ${name}`;
  ```
- **Differences:**
  - **Syntax:** Shorter syntax
  - **this Binding:** Arrow functions do not have their own `this`

---

#### **Slide 6: ES6 Features Overview**
- **Template Literals:**
  - Use backticks (`` ` ``) for string interpolation
  - Multi-line strings
  - Example:
    ```javascript
    const name = 'Alice';
    const message = `Hello, ${name}!`;
    ```
- **Destructuring:**
  - Extract values from arrays or objects
  - Example:
    ```javascript
    const user = { name: 'Bob', age: 25 };
    const { name, age } = user;
    ```
- **Spread Operator:**
  - Expand iterable elements
  - Example:
    ```javascript
    const arr1 = [1, 2, 3];
    const arr2 = [...arr1, 4, 5];
    ```

---

#### **Slide 7: Asynchronous JavaScript**
- **Synchronous vs Asynchronous:**
  - **Synchronous:** Blocking operations
  - **Asynchronous:** Non-blocking, handled via callbacks, promises, or async/await
- **Promises:**
  - Represents future completion of asynchronous operations
  - Example:
    ```javascript
    const fetchData = () => {
      return new Promise((resolve, reject) => {
        // Async operation
      });
    };
    ```
- **Async/Await:**
  - Syntactic sugar over promises
  - Makes asynchronous code look synchronous
  - Example:
    ```javascript
    const getData = async () => {
      try {
        const data = await fetchData();
      } catch (error) {
        console.error(error);
      }
    };
    ```

---

#### **Slide 8: Hands-On Activity Overview**
- **Tasks:**
  1. Write JavaScript snippets utilizing ES6 features
  2. Create a script that fetches data from a public API using async/await

---

#### **Slide 9: Activity Step 1 - JavaScript Utilities Library**
- **Instructions:**
  1. Create a file `utils.js`
  2. Implement the following functions using ES6 features:
     - `add(a, b)` - Returns the sum of two numbers
     - `capitalize(str)` - Capitalizes the first letter of a string
     - `fetchData(url)` - Fetches data from a given API using async/await
  3. Example:
     ```javascript
     // utils.js
     export const add = (a, b) => a + b;

     export const capitalize = (str) => `${str.charAt(0).toUpperCase()}${str.slice(1)}`;

     export const fetchData = async (url) => {
       try {
         const response = await fetch(url);
         const data = await response.json();
         return data;
       } catch (error) {
         console.error('Error fetching data:', error);
       }
     };
     ```
  4. Create a `test.js` to import and test these functions

---

#### **Slide 10: Activity Step 2 - Fetching Data with async/await**
- **Instructions:**
  1. In `test.js`, use the `fetchData` function to get data from [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts)
  2. Example:
     ```javascript
     import { fetchData } from './utils.js';

     const displayPosts = async () => {
       const posts = await fetchData('https://jsonplaceholder.typicode.com/posts');
       console.log(posts);
     };

     displayPosts();
     ```
  3. Run the script using Node.js: `node test.js`
  4. Observe the fetched data in the console

---

#### **Slide 11: Reviewing the Code**
- **Explanation:**
  - **Arrow Functions:** Concise function definitions
  - **Template Literals:** Easier string formatting
  - **Destructuring:** Simplifies extraction of object properties
  - **Spread Operator:** Facilitates array manipulations
  - **Async/Await:** Simplifies asynchronous code handling

---

#### **Slide 12: Best Practices with ES6+**
- **Use `const` by default, `let` when reassignment is needed**
- **Prefer arrow functions for shorter syntax and lexical `this`**
- **Leverage destructuring for cleaner code**
- **Use template literals for string concatenation**
- **Handle asynchronous operations with async/await for readability**

---

#### **Slide 13: Common Pitfalls and How to Avoid Them**
- **Variable Hoisting with `var`:** Leads to unexpected behaviors
- **Incorrect `this` Binding in Traditional Functions**
- **Forgetting to handle promise rejections**
- **Overusing the spread operator leading to performance issues**

---

#### **Slide 14: Summary and Q&A**
- **Recap:**
  - ES6+ introduces significant enhancements to JavaScript
  - Key features include `let`, `const`, arrow functions, template literals, destructuring, spread operator, and async/await
  - Applied these features in practical coding tasks
- **Questions:** Open floor for any student queries

---

### **Module 3: Introduction to Git and Version Control**

---

#### **Slide 1: Title Slide**
- **Title:** Introduction to Git and Version Control
- **Subtitle:** Week 1, Module 3
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the importance of version control
- **Learn** Git basics: init, clone, add, commit, push, pull
- **Master** branching and merging strategies
- **Handle** merge conflicts effectively

---

#### **Slide 3: What is Version Control?**
- **Definition:** System that records changes to files over time
- **Benefits:**
  - Track project history
  - Collaborate with others
  - Revert to previous states
- **Types:**
  - **Centralized (e.g., SVN)**
  - **Distributed (e.g., Git)**

---

#### **Slide 4: Introduction to Git**
- **Definition:** Distributed version control system
- **Key Features:**
  - Branching and merging
  - Distributed nature (each developer has full history)
  - Staging area for commits
- **Why Git?**
  - Widely adopted in the industry
  - Robust and flexible

---

#### **Slide 5: Git Basics Commands**
- **Initialization:**
  - `git init` - Initialize a new Git repository
- **Cloning:**
  - `git clone <repository_url>` - Clone an existing repository
- **Staging and Committing:**
  - `git add <file>` - Stage changes
  - `git commit -m "message"` - Commit changes with a message
- **Pushing and Pulling:**
  - `git push` - Push commits to remote repository
  - `git pull` - Pull updates from remote repository

---

#### **Slide 6: Branching in Git**
- **Purpose:** Isolate work on different features or fixes
- **Commands:**
  - Create a branch: `git branch <branch_name>`
  - Switch to a branch: `git checkout <branch_name>`
  - Create and switch: `git checkout -b <branch_name>`
- **Best Practices:**
  - Use descriptive branch names (e.g., `feature-routing`)
  - Keep branches focused on a single task

---

#### **Slide 7: Merging Branches**
- **Purpose:** Integrate changes from one branch into another
- **Commands:**
  - Switch to target branch: `git checkout main`
  - Merge another branch: `git merge <branch_name>`
- **Fast-Forward vs. Three-Way Merge:**
  - **Fast-Forward:** Linear history, no merge commit
  - **Three-Way:** Creates a merge commit, maintains history

---

#### **Slide 8: Handling Merge Conflicts**
- **What is a Merge Conflict?**
  - Occurs when Git cannot automatically resolve differences between branches
- **Identifying Conflicts:**
  - Git marks conflict areas in affected files
- **Resolving Conflicts:**
  1. Open conflicted files
  2. Decide which changes to keep
  3. Remove conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
  4. Stage the resolved files: `git add <file>`
  5. Commit the merge: `git commit`

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Clone the existing repository from GitHub
  2. Create a new branch `feature-routing`
  3. Implement a new route in Express server
  4. Merge `feature-routing` back into `main`
  5. Resolve any merge conflicts

---

#### **Slide 10: Activity Step 1 - Cloning the Repository**
- **Instructions:**
  1. Open terminal in VS Code
  2. Clone the repository: `git clone <repository_url>`
  3. Navigate into the project directory: `cd fintech-app`
  4. Verify repository setup: `git status`

---

#### **Slide 11: Activity Step 2 - Creating a Feature Branch**
- **Instructions:**
  1. Create and switch to `feature-routing`: `git checkout -b feature-routing`
  2. Confirm branch: `git branch`
  3. Make changes to `server.js` to add a new route `/about`
     ```javascript
     app.get('/about', (req, res) => {
       res.json({ message: 'About Page' });
     });
     ```
  4. Stage and commit changes:
     ```bash
     git add server.js
     git commit -m "Add /about route"
     ```

---

#### **Slide 12: Activity Step 3 - Merging Branches**
- **Instructions:**
  1. Switch to `main` branch: `git checkout main`
  2. Merge `feature-routing`: `git merge feature-routing`
  3. Push changes to GitHub: `git push origin main`
- **Potential Conflicts:** If multiple developers are working, conflicts might arise

---

#### **Slide 13: Activity Step 4 - Resolving Merge Conflicts**
- **Scenario:** Suppose both `main` and `feature-routing` modified the same line in `server.js`
- **Steps to Resolve:**
1. Git notifies about conflicts during merge
2. Open `server.js` to find conflict markers

    ```js
    <<<<<<< HEAD
    res.send('Hello World');
    =======
    res.json({ message: 'About Page' });
    >>>>>>> feature-routing
    ```
3. Decide the correct code, e.g., keep both routes separate
4. Remove conflict markers and adjust code
5. Stage and commit:

    ```bash
    git add server.js
    git commit -m "Resolve merge conflict in server.js"
    ```

---

#### **Slide 14: Best Practices for Git**
- **Commit Often:** Small, frequent commits with meaningful messages
- **Use Branches:** Isolate features, fixes, experiments
- **Pull Before Pushing:** Ensure local repository is up-to-date
- **Write Descriptive Commit Messages:** Clear and concise
- **Avoid Large Binary Files:** Keep repository lightweight

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Importance of version control with Git
  - Basic Git commands and workflows
  - Branching and merging strategies
  - Handling and resolving merge conflicts
- **Questions:** Open floor for any student queries

---

### **Module 4: Introduction to Node.js and Express**

---

#### **Slide 1: Title Slide**
- **Title:** Introduction to Node.js and Express
- **Subtitle:** Week 1, Module 4
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** Node.js architecture
- **Learn** the basics of Express.js framework
- **Set up** an Express server
- **Implement** routing in Express
- **Build** a basic web server with multiple routes

---

#### **Slide 3: Node.js Architecture Overview**
- **Event-Driven:** Handles operations through events and callbacks
- **Single-Threaded:** Uses non-blocking I/O to manage concurrency
- **V8 Engine:** Compiles JavaScript into machine code for performance
- **Modules:** Core, local, and third-party modules

---

#### **Slide 4: What is Express.js?**
- **Definition:** Fast, unopinionated, minimalist web framework for Node.js
- **Features:**
  - Simplifies server and routing management
  - Middleware support
  - Robust API for building web and mobile applications
- **Advantages:**
  - Lightweight and flexible
  - Large ecosystem of middleware and plugins
  - Facilitates rapid development

---

#### **Slide 5: Setting Up an Express Server**
- **Installation:**
  - Initialize npm project: `npm init -y`
  - Install Express: `npm install express`
- **Basic Server Setup:**
  ```javascript
  const express = require('express');
  const app = express();
  const port = 3000;

  app.get('/', (req, res) => {
    res.send('Hello World!');
  });

  app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
  });
  ```

---

#### **Slide 6: Understanding Middleware**
- **Definition:** Functions that execute during the request-response cycle
- **Types:**
  - **Application-level:** `app.use()`, `app.get()`, etc.
  - **Router-level:** Specific to Express routers
  - **Error-handling:** Functions with four arguments `(err, req, res, next)`
- **Examples:**
  ```javascript
  // Application-level middleware
  app.use(express.json());

  // Custom middleware
  app.use((req, res, next) => {
    console.log(`${req.method} ${req.url}`);
    next();
  });
  ```

---

#### **Slide 7: Routing in Express**
- **Definition:** Determines how an application responds to client requests
- **HTTP Methods:** GET, POST, PUT, DELETE, etc.
- **Route Parameters:** Dynamic segments in URLs
- **Examples:**
  ```javascript
  // GET route
  app.get('/users', (req, res) => {
    res.send('List of users');
  });

  // GET with route parameter
  app.get('/users/:id', (req, res) => {
    res.send(`User ID: ${req.params.id}`);
  });

  // POST route
  app.post('/users', (req, res) => {
    res.send('Create a new user');
  });
  ```

---

#### **Slide 8: Hands-On Activity Overview**
- **Tasks:**
  1. Build a basic Express server with multiple routes
  2. Implement middleware for logging incoming requests
  3. Test routes using Postman or a web browser

---

#### **Slide 9: Activity Step 1 - Setting Up Express Server**
- **Instructions:**
  1. Ensure `express` is installed: `npm install express`
  2. Create `server.js` with the basic server setup:
     ```javascript
     const express = require('express');
     const app = express();
     const port = 3000;

     app.get('/', (req, res) => {
       res.send('Hello World!');
     });

     app.get('/api', (req, res) => {
       res.json({ message: 'API Home' });
     });

     app.get('/status', (req, res) => {
       res.json({ status: 'Server is running' });
     });

     app.listen(port, () => {
       console.log(`Server is running on http://localhost:${port}`);
     });
     ```
  3. Run the server: `node server.js`
  4. Access routes in browser or Postman:
     - `http://localhost:3000/`
     - `http://localhost:3000/api`
     - `http://localhost:3000/status`

---

#### **Slide 10: Activity Step 2 - Implementing Middleware**
- **Instructions:**
  1. Add middleware to log incoming requests
     ```javascript
     app.use((req, res, next) => {
       console.log(`${req.method} ${req.url}`);
       next();
     });
     ```
  2. Update `server.js` and restart the server
  3. Observe console logs when accessing different routes

---

#### **Slide 11: Testing Routes with Postman**
- **Instructions:**
  1. Open Postman
  2. Create GET requests to `/`, `/api`, and `/status`
  3. Verify responses:
     - `/` should return "Hello World!"
     - `/api` should return JSON `{ message: 'API Home' }`
     - `/status` should return JSON `{ status: 'Server is running' }`
  4. Experiment with different HTTP methods (e.g., POST to `/api`)

---

#### **Slide 12: Enhancing the Server**
- **Adding More Routes:**
  - Example: `/about` route
    ```javascript
    app.get('/about', (req, res) => {
      res.send('About Page');
    });
    ```
- **Using Route Parameters:**
  - Example: `/users/:id`
    ```javascript
    app.get('/users/:id', (req, res) => {
      res.send(`User ID: ${req.params.id}`);
    });
    ```

---

#### **Slide 13: Live Demonstration**
- **Demonstrate:**
  - Adding a new route
  - Using middleware
  - Testing routes in real-time
- **Encourage Participation:** Ask students to suggest routes or middleware functions

---

#### **Slide 14: Best Practices with Express**
- **Organize Routes:**
  - Use separate modules/files for different routes
- **Use Middleware Effectively:**
  - Utilize built-in and third-party middleware
- **Error Handling:**
  - Implement centralized error handling
- **Security:**
  - Sanitize inputs, use security-related middleware (e.g., helmet)

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Node.js architecture and its asynchronous nature
  - Introduction to Express.js and its features
  - Setting up an Express server with multiple routes
  - Implementing middleware for logging and handling requests
- **Questions:** Open floor for any student queries

---

### **Module 5: Working with npm**

---

#### **Slide 1: Title Slide**
- **Title:** Working with npm (Node Package Manager)
- **Subtitle:** Week 1, Module 5
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the role of npm in Node.js projects
- **Learn** to manage dependencies with `package.json`
- **Master** installing and updating packages
- **Utilize** npm scripts for automation
- **Administer** basic project configurations and maintenance

---

#### **Slide 3: Introduction to npm**
- **Definition:** Default package manager for Node.js
- **Functions:**
  - Install and manage project dependencies
  - Share and reuse code packages
  - Automate development tasks through scripts
- **Key Features:**
  - Vast repository of packages (npm registry)
  - Semantic versioning for package versions

---

#### **Slide 4: Understanding package.json**
- **Purpose:** Central file managing project metadata and dependencies
- **Key Fields:**
  - `name`: Project name
  - `version`: Project version
  - `scripts`: Custom commands for automation
  - `dependencies`: Production dependencies
  - `devDependencies`: Development-only dependencies
- **Example:**
  ```json
  {
    "name": "fintech-app",
    "version": "1.0.0",
    "scripts": {
      "start": "node server.js",
      "dev": "nodemon server.js"
    },
    "dependencies": {
      "express": "^4.17.1",
      "morgan": "^1.10.0"
    },
    "devDependencies": {
      "nodemon": "^2.0.7"
    }
  }
  ```

---

#### **Slide 5: Installing and Managing Dependencies**
- **Installing Packages:**
  - Local installation: `npm install <package_name>` (adds to `dependencies`)
  - Development installation: `npm install <package_name> --save-dev` (adds to `devDependencies`)
- **Example:**
  ```bash
  npm install morgan --save
  npm install nodemon --save-dev
  ```
- **Updating Packages:**
  - Update all packages: `npm update`
  - Update specific package: `npm update <package_name>`

---

#### **Slide 6: Semantic Versioning (SemVer)**
- **Format:** `MAJOR.MINOR.PATCH`
  - **MAJOR:** Incompatible API changes
  - **MINOR:** Backwards-compatible functionality
  - **PATCH:** Backwards-compatible bug fixes
- **Example:**
  - `"express": "^4.17.1"`
    - `^` allows updates that do not modify the left-most non-zero digit (e.g., up to `<5.0.0`)

---

#### **Slide 7: npm Scripts for Automation**
- **Purpose:** Automate repetitive tasks (e.g., starting server, testing)
- **Common Scripts:**
  - `start`: Start the application
  - `test`: Run tests
  - `dev`: Start development server with tools like nodemon
- **Example:**
  ```json
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "test": "jest"
  }
  ```

---

#### **Slide 8: Creating Custom npm Scripts**
- **Example Task:** Run a linter or build tool
- **Example:**
  ```json
  "scripts": {
    "lint": "eslint .",
    "build": "webpack --config webpack.config.js"
  }
  ```
- **Running Scripts:**
  - `npm run <script_name>` (e.g., `npm run lint`)

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Initialize a new npm project
  2. Install necessary packages (`morgan`, `dotenv`)
  3. Manage package versions and dependencies
  4. Create custom npm scripts for the project

---

#### **Slide 10: Activity Step 1 - Initializing npm Project**
- **Instructions:**
  1. Open terminal in VS Code
  2. Navigate to project directory: `cd fintech-app`
  3. Initialize npm: `npm init -y` (creates `package.json` with default settings)
  4. Review and edit `package.json` as needed

---

#### **Slide 11: Activity Step 2 - Installing Packages**
- **Instructions:**
  1. Install `morgan` for logging:
     ```bash
     npm install morgan --save
     ```
  2. Install `dotenv` for environment variables:
     ```bash
     npm install dotenv --save
     ```
  3. Install `nodemon` for development:
     ```bash
     npm install nodemon --save-dev
     ```

---

#### **Slide 12: Activity Step 3 - Managing package.json**
- **Tasks:**
  1. Add custom scripts:
     ```json
     "scripts": {
       "start": "node server.js",
       "dev": "nodemon server.js",
       "lint": "eslint ."
     }
     ```
  2. Ensure dependencies are listed correctly
  3. Create a `.gitignore` file to exclude `node_modules/` and `.env`

---

#### **Slide 13: Activity Step 4 - Creating Custom npm Scripts**
- **Instructions:**
  1. Add a `start` script to run the server
  2. Add a `dev` script to run the server with nodemon for automatic restarts
  3. Example:
     ```json
     "scripts": {
       "start": "node server.js",
       "dev": "nodemon server.js"
     }
     ```
  4. Run the development server: `npm run dev`

---

#### **Slide 14: Best Practices with npm**
- **Maintain Clean `package.json`:**
  - Remove unused dependencies
  - Use exact versions when necessary
- **Use Semantic Versioning Appropriately**
- **Leverage Scripts for Automation:**
  - Testing, linting, building, deploying
- **Regularly Update Dependencies:**
  - Keep packages up-to-date for security and performance

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Role and importance of npm in Node.js projects
  - Managing dependencies with `package.json`
  - Installing, updating, and organizing packages
  - Automating tasks with npm scripts
- **Questions:** Open floor for any student queries

---

## **Week 2: Backend Development with Node.js and MySQL**

### **Module 6: Introduction to MySQL**

---

#### **Slide 1: Title Slide**
- **Title:** Introduction to MySQL
- **Subtitle:** Week 2, Module 6
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** relational databases vs. NoSQL
- **Learn** to set up and configure MySQL
- **Master** basic SQL commands: SELECT, INSERT, UPDATE, DELETE
- **Design** a simple database schema for the Financial application

---

#### **Slide 3: Relational Databases vs. NoSQL**
- **Relational Databases (RDBMS):**
  - Structured data in tables with predefined schemas
  - Use SQL for queries
  - Examples: MySQL, PostgreSQL, Oracle
- **NoSQL Databases:**
  - Flexible, schema-less data storage
  - Suitable for unstructured data
  - Examples: MongoDB, Cassandra, Redis
- **Use Cases:**
  - RDBMS: Financial applications requiring transactions and data integrity
  - NoSQL: Real-time applications, large-scale data storage

---

#### **Slide 4: Introduction to MySQL**
- **Definition:** Open-source relational database management system
- **Features:**
  - ACID compliance for reliable transactions
  - Supports complex queries and joins
  - Scalable and flexible
- **Why MySQL for FinTech:**
  - Ensures data integrity and security
  - Efficient handling of transactional data

---

#### **Slide 5: Setting Up MySQL**
- **Installation:**
  - Download from [MySQL Downloads](https://dev.mysql.com/downloads/)
  - Choose community edition for free usage
  - Follow installation wizard instructions
- **Configuration:**
  - Set root password
  - Configure port (default: 3306)
  - Secure installation with `mysql_secure_installation`
- **Accessing MySQL:**
  - Using Command Line: `mysql -u root -p`
  - Using GUI tools: MySQL Workbench, phpMyAdmin

---

#### **Slide 6: Basic SQL Commands**
- **SELECT:** Retrieve data from tables
  ```sql
  SELECT * FROM users;
  SELECT name, email FROM users WHERE id = 1;
  ```
- **INSERT:** Add new records
  ```sql
  INSERT INTO users (name, email, password) VALUES ('Alice', 'alice@example.com', 'password123');
  ```
- **UPDATE:** Modify existing records
  ```sql
  UPDATE users SET email = 'alice_new@example.com' WHERE id = 1;
  ```
- **DELETE:** Remove records
  ```sql
  DELETE FROM users WHERE id = 1;
  ```

---

#### **Slide 7: Designing a Simple Database Schema**
- **Entities for Financial Application:**
  - **Users:** User information and authentication
  - **Accounts:** Financial accounts linked to users
  - **Transactions:** Financial transactions associated with accounts
- **Relationships:**
  - **One-to-Many:** One user can have multiple accounts
  - **One-to-Many:** One account can have multiple transactions
- **ER Diagram:**
  - **Users** ↔ **Accounts** ↔ **Transactions**

---

#### **Slide 8: Creating Tables in MySQL**
- **Users Table:**
  ```sql
  CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
  );
  ```
- **Accounts Table:**
  ```sql
  CREATE TABLE accounts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    account_type VARCHAR(50),
    balance DECIMAL(10,2) DEFAULT 0.00,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
  );
  ```
- **Transactions Table:**
  ```sql
  CREATE TABLE transactions (
    id INT AUTO_INCREMENT PRIMARY KEY,
    account_id INT,
    type ENUM('credit', 'debit') NOT NULL,
    amount DECIMAL(10,2) NOT NULL,
    description VARCHAR(255),
    transaction_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (account_id) REFERENCES accounts(id)
  );
  ```

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Install and set up MySQL
  2. Create a new database `fintech_app`
  3. Design and create `users`, `accounts`, and `transactions` tables
  4. Insert sample data into the tables
  5. Execute basic SQL queries for CRUD operations

---

#### **Slide 10: Activity Step 1 - Creating the Database**
- **Instructions:**
  1. Open MySQL command line or MySQL Workbench
  2. Create database:
     ```sql
     CREATE DATABASE fintech_app;
     USE fintech_app;
     ```
  3. Verify creation: `SHOW DATABASES;`

---

#### **Slide 11: Activity Step 2 - Creating Tables**
- **Instructions:**
  1. Create `users` table:
     ```sql
     CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       email VARCHAR(100) UNIQUE NOT NULL,
       password VARCHAR(255) NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```
  2. Create `accounts` table:
     ```sql
     CREATE TABLE accounts (
       id INT AUTO_INCREMENT PRIMARY KEY,
       user_id INT,
       account_type VARCHAR(50),
       balance DECIMAL(10,2) DEFAULT 0.00,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (user_id) REFERENCES users(id)
     );
     ```
  3. Create `transactions` table:
     ```sql
     CREATE TABLE transactions (
       id INT AUTO_INCREMENT PRIMARY KEY,
       account_id INT,
       type ENUM('credit', 'debit') NOT NULL,
       amount DECIMAL(10,2) NOT NULL,
       description VARCHAR(255),
       transaction_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (account_id) REFERENCES accounts(id)
     );
     ```
  4. Verify tables: `SHOW TABLES;`

---

#### **Slide 12: Activity Step 3 - Inserting Sample Data**
- **Instructions:**
  1. Insert into `users`:
     ```sql
     INSERT INTO users (name, email, password) VALUES
     ('Alice Johnson', 'alice@example.com', 'hashedpassword1'),
     ('Bob Smith', 'bob@example.com', 'hashedpassword2');
     ```
  2. Insert into `accounts`:
     ```sql
     INSERT INTO accounts (user_id, account_type, balance) VALUES
     (1, 'Checking', 1500.00),
     (1, 'Savings', 5000.00),
     (2, 'Checking', 2000.00);
     ```
  3. Insert into `transactions`:
     ```sql
     INSERT INTO transactions (account_id, type, amount, description) VALUES
     (1, 'credit', 500.00, 'Salary'),
     (1, 'debit', 100.00, 'Groceries'),
     (2, 'credit', 2000.00, 'Investment Return');
     ```

---

#### **Slide 13: Activity Step 4 - Executing CRUD Operations**
- **SELECT Examples:**
  ```sql
  SELECT * FROM users;
  SELECT name, email FROM users WHERE id = 1;
  ```
- **UPDATE Example:**
  ```sql
  UPDATE accounts SET balance = balance + 500.00 WHERE id = 1;
  ```
- **DELETE Example:**
  ```sql
  DELETE FROM transactions WHERE id = 3;
  ```
- **Hands-On:**
  - Execute the above queries and observe changes

---

#### **Slide 14: Best Practices in Database Design**
- **Normalization:**
  - Eliminate data redundancy
  - Organize tables and relationships logically
- **Use Appropriate Data Types:**
  - Choose data types that best represent the data
- **Indexing:**
  - Improve query performance with indexes on frequently searched columns
- **Security:**
  - Use proper authentication and authorization
  - Encrypt sensitive data

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Differences between relational and NoSQL databases
  - Setting up and configuring MySQL
  - Creating and managing databases and tables
  - Performing basic CRUD operations with SQL
- **Questions:** Open floor for any student queries

---

### **Module 7: Data Modeling and ORM with Sequelize**

---

#### **Slide 1: Title Slide**
- **Title:** Data Modeling and ORM with Sequelize
- **Subtitle:** Week 2, Module 7
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the concept of ORM (Object-Relational Mapping)
- **Learn** to set up Sequelize with Node.js
- **Define** models and relationships using Sequelize
- **Perform** CRUD operations using Sequelize methods

---

#### **Slide 3: What is ORM?**
- **Definition:** Technique to convert data between incompatible type systems using object-oriented programming languages
- **Benefits:**
  - Simplifies database interactions
  - Reduces the need for raw SQL queries
  - Enhances code maintainability and readability
- **Popular ORMs:** Sequelize (Node.js), Entity Framework (.NET), Hibernate (Java)

---

#### **Slide 4: Introduction to Sequelize**
- **Definition:** Promise-based Node.js ORM for relational databases (supports MySQL, PostgreSQL, SQLite, MSSQL)
- **Features:**
  - Model definitions and associations
  - Migration and seeding support
  - Querying and transactions
- **Advantages:**
  - Abstracts SQL queries
  - Provides a consistent API across different databases
  - Supports advanced features like eager loading and associations

---

#### **Slide 5: Setting Up Sequelize**
- **Installation:**
  ```bash
  npm install sequelize sequelize-cli mysql2 --save
  ```
- **Initialization:**
  ```bash
  npx sequelize-cli init
  ```
  - Creates folders: `config`, `models`, `migrations`, `seeders`
- **Configuration:**
  - Update `config/config.json` with MySQL credentials
    ```json
    {
      "development": {
        "username": "root",
        "password": "your_password",
        "database": "fintech_app",
        "host": "127.0.0.1",
        "dialect": "mysql"
      }
    }
    ```

---

#### **Slide 6: Defining Models with Sequelize**
- **Model Structure:**
  - **Attributes:** Define table columns and data types
  - **Associations:** Define relationships between models
- **Example: Defining User Model**
  ```javascript
  // models/user.js
  module.exports = (sequelize, DataTypes) => {
    const User = sequelize.define('User', {
      name: {
        type: DataTypes.STRING,
        allowNull: false
      },
      email: {
        type: DataTypes.STRING,
        unique: true,
        allowNull: false
      },
      password: {
        type: DataTypes.STRING,
        allowNull: false
      }
    }, {});

    User.associate = function(models) {
      User.hasMany(models.Account, { foreignKey: 'userId', as: 'accounts' });
    };

    return User;
  };
  ```

---

#### **Slide 7: Defining Associations**
- **One-to-Many Relationship:**
  - One User has many Accounts
  - One Account has many Transactions
- **Example: Defining Account Model**
  ```javascript
  // models/account.js
  module.exports = (sequelize, DataTypes) => {
    const Account = sequelize.define('Account', {
      accountType: {
        type: DataTypes.STRING,
        allowNull: false
      },
      balance: {
        type: DataTypes.DECIMAL(10,2),
        defaultValue: 0.00
      }
    }, {});

    Account.associate = function(models) {
      Account.belongsTo(models.User, { foreignKey: 'userId', as: 'user' });
      Account.hasMany(models.Transaction, { foreignKey: 'accountId', as: 'transactions' });
    };

    return Account;
  };
  ```
---
#### **Slide 7.1: Defining Associations**
- **Example: Defining Transaction Model**
  ```javascript
  // models/transaction.js
  module.exports = (sequelize, DataTypes) => {
    const Transaction = sequelize.define('Transaction', {
      type: {
        type: DataTypes.ENUM('credit', 'debit'),
        allowNull: false
      },
      amount: {
        type: DataTypes.DECIMAL(10,2),
        allowNull: false
      },
      description: {
        type: DataTypes.STRING
      }
    }, {});

    Transaction.associate = function(models) {
      Transaction.belongsTo(models.Account, { foreignKey: 'accountId', as: 'account' });
    };

    return Transaction;
  };
  ```

---

#### **Slide 8: Performing CRUD Operations with Sequelize**
- **Create:**
  ```javascript
  const newUser = await User.create({
    name: 'Charlie Brown',
    email: 'charlie@example.com',
    password: 'securepassword'
  });
  ```
- **Read:**
  ```javascript
  const users = await User.findAll();
  const user = await User.findOne({ where: { email: 'alice@example.com' } });
  ```
- **Update:**
  ```javascript
  const user = await User.findByPk(1);
  user.name = 'Alice Wonderland';
  await user.save();
  ```
- **Delete:**
  ```javascript
  const user = await User.findByPk(2);
  await user.destroy();
  ```

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Install and configure Sequelize with MySQL
  2. Define Sequelize models for `User`, `Account`, and `Transaction`
  3. Sync models with the database
  4. Perform CRUD operations using Sequelize
  5. Commit the integration and model definitions to Git

---

#### **Slide 10: Activity Step 1 - Installing and Configuring Sequelize**
- **Instructions:**
  1. Install Sequelize and dependencies:
     ```bash
     npm install sequelize sequelize-cli mysql2 --save
     ```
  2. Initialize Sequelize:
     ```bash
     npx sequelize-cli init
     ```
  3. Configure `config/config.json` with MySQL credentials

---

#### **Slide 11: Activity Step 2 - Defining Models**
- **Instructions:**
  1. Create `User`, `Account`, and `Transaction` models as per previous examples
  2. Define associations in each model file
  3. Ensure models are exported correctly

---

#### **Slide 12: Activity Step 3 - Syncing Models with Database**
- **Instructions:**
  1. Create migrations for each model using Sequelize CLI:
     ```bash
     npx sequelize-cli model:generate --name User --attributes name:string,email:string,password:string
     npx sequelize-cli model:generate --name Account --attributes accountType:string,balance:decimal,userId:integer
     npx sequelize-cli model:generate --name Transaction --attributes type:enum,amount:decimal,description:string,accountId:integer
     ```
  2. Review and adjust migration files as needed
  3. Run migrations to create tables:
     ```bash
     npx sequelize-cli db:migrate
     ```
  4. Verify tables in MySQL

---

#### **Slide 13: Activity Step 4 - Performing CRUD Operations**
- **Instructions:**
  1. Create a script `crud.js` to perform CRUD operations
  2. Example:
     ```javascript
     const { User, Account, Transaction, sequelize } = require('./models');

     const performCRUD = async () => {
       try {
         // Create
         const user = await User.create({
           name: 'David Lee',
           email: 'david@example.com',
           password: 'password456'
         });

         // Read
         const users = await User.findAll();
         console.log(users);

         // Update
         user.name = 'David Beckham';
         await user.save();

         // Delete
         await user.destroy();

         await sequelize.close();
       } catch (error) {
         console.error(error);
       }
     };

     performCRUD();
     ```
  3. Run the script: `node crud.js`
  4. Observe changes in the database

---

#### **Slide 14: Best Practices with Sequelize**
- **Use Migrations:**
  - Keep database schema changes trackable and reversible
- **Define Associations Clearly:**
  - Ensure correct relationships between models
- **Handle Errors Gracefully:**
  - Use try-catch blocks and proper error handling
- **Secure Sensitive Data:**
  - Hash passwords before storing
- **Optimize Queries:**
  - Use eager loading to minimize database calls

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Understanding ORM and benefits of Sequelize
  - Setting up Sequelize with MySQL
  - Defining models and their associations
  - Performing CRUD operations using Sequelize methods
- **Questions:** Open floor for any student queries

---

### **Module 8: Building RESTful APIs with Express**

---

#### **Slide 1: Title Slide**
- **Title:** Building RESTful APIs with Express
- **Subtitle:** Week 2, Module 8
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** principles of RESTful API design
- **Learn** to create API endpoints using Express
- **Implement** middleware for logging, validation, and error handling
- **Handle** errors and validate requests effectively

---

#### **Slide 3: Principles of RESTful API Design**
- **Stateless:** Each request contains all necessary information
- **Client-Server Architecture:** Separation of concerns
- **Uniform Interface:** Consistent use of HTTP methods and status codes
- **Resource-Based:** Manipulate resources via URIs
- **Representations:** Use JSON or XML to represent resources

---

#### **Slide 4: RESTful API Endpoints**
- **Standard HTTP Methods:**
  - **GET:** Retrieve data
  - **POST:** Create new data
  - **PUT/PATCH:** Update existing data
  - **DELETE:** Remove data
- **Endpoint Structure:**
  - `/users` - GET, POST
  - `/users/:id` - GET, PUT, DELETE
  - `/accounts` - GET, POST
  - `/accounts/:id` - GET, PUT, DELETE

---

#### **Slide 5: Middleware in Express**
- **Definition:** Functions that have access to request and response objects
- **Types:**
  - **Built-in Middleware:** `express.json()`, `express.urlencoded()`
  - **Third-Party Middleware:** `morgan`, `cors`
  - **Custom Middleware:** Logging, authentication
- **Usage:**
  ```javascript
  app.use(express.json());
  app.use(morgan('dev'));
  ```

---

#### **Slide 6: Error Handling and Validation**
- **Error Handling:**
  - Centralized error handling middleware
  - Send appropriate HTTP status codes and messages
  - Example:
    ```javascript
    app.use((err, req, res, next) => {
      console.error(err.stack);
      res.status(500).json({ error: 'Something went wrong!' });
    });
    ```
- **Validation:**
  - Validate incoming data using libraries like `express-validator` or custom middleware
  - Ensure data integrity and prevent invalid data from being processed

---

#### **Slide 7: Building RESTful API Endpoints**
- **Example: Users API**
  - **POST /users:** Create a new user
  - **GET /users/:id:** Retrieve a specific user
  - **PUT /users/:id:** Update a specific user
  - **DELETE /users/:id:** Delete a specific user
- **Example Code:**
  ```javascript
  // Create User
  app.post('/users', async (req, res, next) => {
    try {
      const user = await User.create(req.body);
      res.status(201).json(user);
    } catch (error) {
      next(error);
    }
  });

  // Get User by ID
  app.get('/users/:id', async (req, res, next) => {
    try {
      const user = await User.findByPk(req.params.id, { include: ['accounts'] });
      if (user) {
        res.json(user);
      } else {
        res.status(404).json({ error: 'User not found' });
      }
    } catch (error) {
      next(error);
    }
  });
  ```

---

#### **Slide 8: Hands-On Activity Overview**
- **Tasks:**
  1. Develop RESTful API endpoints for Users, Accounts, and Transactions
  2. Implement middleware for request validation and error handling
  3. Test all endpoints using Postman

---

#### **Slide 9: Activity Step 1 - Creating API Endpoints**
- **Instructions:**
  1. Define routes for `users`, `accounts`, and `transactions`
  2. Example: Users routes in `routes/users.js`
  3. Integrate routes in `server.js`:

     ```javascript
     const express = require('express');
     const router = express.Router();
     const { User } = require('../models');

     // Create User
     router.post('/', async (req, res, next) => {
       try {
         const user = await User.create(req.body);
         res.status(201).json(user);
       } catch (error) {
         next(error);
       }
     });

     // Get User by ID
     router.get('/:id', async (req, res, next) => {
       try {
         const user = await User.findByPk(req.params.id, { include: ['accounts'] });
         if (user) {
           res.json(user);
         } else {
           res.status(404).json({ error: 'User not found' });
         }
       } catch (error) {
         next(error);
       }
     });
     ```
---

#### **Slide 9: Activity Step 1.1 - Creating API Endpoints**
     ```javascript
     // Update User
     router.put('/:id', async (req, res, next) => {
       try {
         const user = await User.findByPk(req.params.id);
         if (user) {
           await user.update(req.body);
           res.json(user);
         } else {
           res.status(404).json({ error: 'User not found' });
         }
       } catch (error) {
         next(error);
       }
     });
     ```
---

#### **Slide 9: Activity Step 1.2 - Creating API Endpoints**
```javascript
     // Delete User
     router.delete('/:id', async (req, res, next) => {
       try {
         const user = await User.findByPk(req.params.id);
         if (user) {
           await user.destroy();
           res.json({ message: 'User deleted' });
         } else {
           res.status(404).json({ error: 'User not found' });
         }
       } catch (error) {
         next(error);
       }
     });

     module.exports = router;
  ```
---

#### **Slide 9: Activity Step 1.3 - Creating API Endpoints**
  ```js
     const userRoutes = require('./routes/users');
     app.use('/users', userRoutes);
  ```
---

#### **Slide 10: Activity Step 2 - Implementing Middleware**
- **Instructions:**
  1. Install `express-validator` for request validation:
     ```bash
     npm install express-validator --save
     ```
  2. Add validation to `POST /users` route:
     ```javascript
     const { body, validationResult } = require('express-validator');

     router.post('/', [
       body('name').notEmpty().withMessage('Name is required'),
       body('email').isEmail().withMessage('Valid email is required'),
       body('password').isLength({ min: 6 }).withMessage('Password must be at least 6 characters')
     ], async (req, res, next) => {
       const errors = validationResult(req);
       if (!errors.isEmpty()) {
         return res.status(400).json({ errors: errors.array() });
       }
       try {
         const user = await User.create(req.body);
         res.status(201).json(user);
       } catch (error) {
         next(error);
       }
     });
     ```
  3. Implement centralized error handling middleware in `server.js`:
     ```javascript
     app.use((err, req, res, next) => {
       console.error(err.stack);
       res.status(500).json({ error: 'Internal Server Error' });
     });
     ```

---

#### **Slide 11: Activity Step 3 - Testing Endpoints with Postman**
- **Instructions:**
  1. Open Postman and create requests for each endpoint:
     - **POST /users:** Create a new user
     - **GET /users/:id:** Retrieve a user by ID
     - **PUT /users/:id:** Update a user
     - **DELETE /users/:id:** Delete a user
  2. **Testing Validations:**
     - Try creating a user without a name or with an invalid email to see validation errors
  3. **Observing Responses:**
     - Successful operations return appropriate status codes and data
     - Errors return meaningful messages

---

#### **Slide 12: API Documentation**
- **Importance:** Clear documentation aids developers in using the API
- **Tools:**
  - **Swagger:** Interactive API documentation
  - **Postman Collections:** Shareable API test suites
  - **README Files:** Basic documentation for endpoints
- **Example: Simple README Documentation**
  ```markdown
  # FinTech App API

  ## Users

  - **POST /users**
    - Create a new user
    - **Body:**
      ```json
      {
        "name": "Alice",
        "email": "alice@example.com",
        "password": "password123"
      }
      ```
    - **Responses:**
      - `201 Created` with user data
      - `400 Bad Request` with validation errors

  - **GET /users/:id**
    - Retrieve a user by ID
    - **Responses:**
      - `200 OK` with user data
      - `404 Not Found` if user does not exist
  ```
  
---

#### **Slide 13: Best Practices for RESTful APIs**
- **Use Proper HTTP Status Codes:**
  - `200 OK`, `201 Created`, `400 Bad Request`, `404 Not Found`, `500 Internal Server Error`
- **Consistent Naming Conventions:**
  - Use plural nouns for resources (e.g., `/users`, `/accounts`)
- **Versioning:**
  - Include API version in the URL (e.g., `/api/v1/users`)
- **Security:**
  - Implement authentication and authorization
  - Validate and sanitize inputs to prevent injections

---

#### **Slide 14: Common Pitfalls and How to Avoid Them**
- **Lack of Validation:** Always validate incoming data
- **Poor Error Handling:** Provide meaningful error messages and status codes
- **Inconsistent Endpoints:** Maintain uniformity in endpoint naming and structure
- **Ignoring Security:** Protect endpoints with proper authentication and authorization

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Principles of RESTful API design
  - Creating and managing API endpoints with Express
  - Implementing middleware for validation and error handling
  - Testing APIs effectively with Postman
- **Questions:** Open floor for any student queries

---

### **Module 9: Authentication and Authorization**

---

#### **Slide 1: Title Slide**
- **Title:** Authentication and Authorization
- **Subtitle:** Week 2, Module 9
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the importance of security in web applications
- **Learn** to implement user authentication using JWT (JSON Web Tokens)
- **Protect** API routes to ensure only authenticated access
- **Hash** passwords securely with bcrypt

---

#### **Slide 3: Importance of Security in Web Applications**
- **Data Protection:** Safeguard sensitive user information
- **Prevent Unauthorized Access:** Ensure only authorized users can access certain resources
- **Maintain Trust:** Users trust applications that secure their data
- **Compliance:** Meet legal and regulatory requirements

---

#### **Slide 4: What is Authentication?**
- **Definition:** Process of verifying a user's identity
- **Common Methods:**
  - Username and password
  - OAuth (e.g., Google, Facebook login)
  - Multi-factor authentication (MFA)
- **Tokens vs. Sessions:**
  - **Tokens (JWT):** Stateless, scalable
  - **Sessions:** Server-side storage, require scalability management

---

#### **Slide 5: What is Authorization?**
- **Definition:** Process of determining if a user has permission to access a resource
- **Role-Based Access Control (RBAC):**
  - Assign roles to users and define permissions per role
- **Example:**
  - **Admin:** Can create, read, update, delete all resources
  - **User:** Can read and update own resources

---

#### **Slide 6: Introduction to JWT (JSON Web Tokens)**
- **Definition:** Compact, URL-safe means of representing claims to be transferred between two parties
- **Structure:**
  - **Header:** Specifies token type and hashing algorithm
  - **Payload:** Contains claims (user data, permissions)
  - **Signature:** Ensures token integrity
- **Flow:**
  1. User authenticates
  2. Server generates JWT
  3. Client stores JWT (e.g., localStorage)
  4. Client sends JWT with subsequent requests
  5. Server verifies JWT and grants access

---

#### **Slide 7: Hashing Passwords with bcrypt**
- **Definition:** Password hashing function that incorporates salt to protect against rainbow table attacks
- **Advantages:**
  - Securely stores passwords
  - Resistant to brute-force attacks
- **Example Usage:**
  ```javascript
  const bcrypt = require('bcrypt');
  const saltRounds = 10;
  const password = 'password123';

  bcrypt.hash(password, saltRounds, function(err, hash) {
    // Store hash in database
  });

  // Comparing password
  bcrypt.compare(password, hash, function(err, result) {
    if (result) {
      // Passwords match
    } else {
      // Passwords do not match
    }
  });
  ```

---

#### **Slide 8: Implementing User Authentication with JWT**
- **Steps:**
  1. User registers with email and password
  2. Password is hashed and stored
  3. User logs in with credentials
  4. Server verifies credentials and generates JWT
  5. JWT is sent to the client
  6. Client stores JWT and includes it in authorization headers for protected routes

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Install and configure `jsonwebtoken` and `bcrypt`
  2. Create user registration and login endpoints
  3. Implement password hashing with bcrypt
  4. Generate and verify JWT tokens
  5. Protect specific API routes with JWT verification

---

#### **Slide 10: Activity Step 1 - Installing Dependencies**
- **Instructions:**
  1. Install `jsonwebtoken` and `bcrypt`:
     ```bash
     npm install jsonwebtoken bcrypt --save
     ```
  2. Require them in `routes/auth.js`:
     ```javascript
     const jwt = require('jsonwebtoken');
     const bcrypt = require('bcrypt');
     ```

---

#### **Slide 11: Activity Step 2 - Creating Registration Endpoint**
- **Instructions:**
  1. Create `routes/auth.js`
  2. Implement `POST /auth/register`:
     ```javascript
     const express = require('express');
     const router = express.Router();
     const bcrypt = require('bcrypt');
     const { User } = require('../models');

     router.post('/register', async (req, res, next) => {
       try {
         const { name, email, password } = req.body;
         const hashedPassword = await bcrypt.hash(password, 10);
         const user = await User.create({ name, email, password: hashedPassword });
         res.status(201).json({ message: 'User registered successfully' });
       } catch (error) {
         next(error);
       }
     });

     module.exports = router;
     ```
  3. Integrate `auth` routes in `server.js`:
     ```javascript
     const authRoutes = require('./routes/auth');
     app.use('/auth', authRoutes);
     ```

---

#### **Slide 12: Activity Step 3 - Creating Login Endpoint**
- **Instructions:**
  1. Implement `POST /auth/login` in `routes/auth.js`:
     ```javascript
     const jwt = require('jsonwebtoken');

     router.post('/login', async (req, res, next) => {
       try {
         const { email, password } = req.body;
         const user = await User.findOne({ where: { email } });
         if (!user) {
           return res.status(400).json({ error: 'Invalid credentials' });
         }

         const isMatch = await bcrypt.compare(password, user.password);
         if (!isMatch) {
           return res.status(400).json({ error: 'Invalid credentials' });
         }

         const token = jwt.sign({ id: user.id, email: user.email }, 'your_jwt_secret', { expiresIn: '1h' });
         res.json({ token });
       } catch (error) {
         next(error);
       }
     });
     ```
  2. Replace `'your_jwt_secret'` with an environment variable for security

---

#### **Slide 13: Activity Step 4 - Protecting API Routes**
- **Instructions:**
  1. Create authentication middleware `middleware/auth.js`:
     ```javascript
     const jwt = require('jsonwebtoken');

     const authenticateToken = (req, res, next) => {
       const authHeader = req.headers['authorization'];
       const token = authHeader && authHeader.split(' ')[1];

       if (token == null) return res.status(401).json({ error: 'No token provided' });

       jwt.verify(token, 'your_jwt_secret', (err, user) => {
         if (err) return res.status(403).json({ error: 'Invalid token' });
         req.user = user;
         next();
       });
     };

     module.exports = authenticateToken;
     ```
  2. Protect routes by adding middleware:
     ```javascript
     const authenticateToken = require('../middleware/auth');

     router.get('/profile', authenticateToken, async (req, res, next) => {
       try {
         const user = await User.findByPk(req.user.id, { include: ['accounts'] });
         res.json(user);
       } catch (error) {
         next(error);
       }
     });
     ```
  3. Test protected routes by including `Authorization: Bearer <token>` header in requests

---

#### **Slide 14: Best Practices for Authentication and Authorization**
- **Secure JWT Secrets:**
  - Store secrets in environment variables, not in code
- **Token Expiration:**
  - Set appropriate expiration times for tokens
- **Refresh Tokens:**
  - Implement refresh tokens for prolonged sessions
- **Password Security:**
  - Always hash and salt passwords
  - Enforce strong password policies
- **Use HTTPS:**
  - Encrypt data in transit

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Importance of authentication and authorization
  - Implementing user registration and login with bcrypt and JWT
  - Protecting API routes to ensure secure access
  - Best practices for maintaining security in web applications
- **Questions:** Open floor for any student queries

---

### **Module 10: Integrating Frontend with Backend**

---

#### **Slide 1: Title Slide**
- **Title:** Integrating Frontend with Backend
- **Subtitle:** Week 2, Module 10
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** RESTful communication between frontend and backend
- **Learn** to use the Fetch API in Vanilla JavaScript
- **Handle** CORS (Cross-Origin Resource Sharing)
- **Consume** API data in the frontend application

---

#### **Slide 3: RESTful Communication Overview**
- **Client-Server Model:**
  - Frontend (Client) interacts with backend (Server) via HTTP requests
- **Data Exchange:**
  - Typically in JSON format
- **Flow:**
  1. User interacts with frontend (e.g., submits a form)
  2. Frontend sends HTTP request to backend API
  3. Backend processes request and sends response
  4. Frontend updates UI based on response

---

#### **Slide 4: Introduction to Fetch API**
- **Definition:** Modern interface for making HTTP requests in the browser
- **Features:**
  - Returns promises
  - Supports various HTTP methods
  - Easy to use with async/await
- **Basic Usage:**
  ```javascript
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));
  ```
- **With Async/Await:**
  ```javascript
  const getData = async () => {
    try {
      const response = await fetch('https://api.example.com/data');
      const data = await response.json();
      console.log(data);
    } catch (error) {
      console.error(error);
    }
  };
  ```

---

#### **Slide 5: Handling CORS in Express**
- **What is CORS?**
  - Security feature that restricts web pages from making requests to a different domain
- **Problem:** Frontend and backend may run on different origins (e.g., different ports)
- **Solution:**
  - Enable CORS on the backend to allow cross-origin requests
- **Using `cors` Middleware:**
  ```bash
  npm install cors --save
  ```
  ```javascript
  const cors = require('cors');
  app.use(cors());
  ```
- **Configuration:**
  - Allow specific origins, methods, and headers as needed

---

#### **Slide 6: Consuming API Data in Frontend**
- **Steps:**
  1. Make HTTP request using Fetch API
  2. Handle the response data
  3. Update the DOM to display data
- **Example: Fetching User Data**
  ```javascript
  const fetchUser = async () => {
    try {
      const response = await fetch('http://localhost:3000/users/1', {
        headers: {
          'Authorization': 'Bearer <token>'
        }
      });
      const user = await response.json();
      document.getElementById('user-name').textContent = user.name;
      document.getElementById('user-email').textContent = user.email;
    } catch (error) {
      console.error('Error fetching user:', error);
    }
  };

  fetchUser();
  ```

---

#### **Slide 7: Hands-On Activity Overview**
- **Tasks:**
  1. Create frontend forms for user registration and login
  2. Use Fetch API to handle form submissions
  3. Display success and error messages based on API responses
  4. Implement CORS handling on the backend

---

#### **Slide 8: Activity Step 1 - Creating Frontend Forms**
- **Instructions:**
1. Create `index.html` with registration and login forms
  ```html
      <!DOCTYPE html>
      <html>
      <head>
        <title>FinTech App</title>
      </head>
      <body>
        <h1>Register</h1>
        <form id="register-form">
          <input type="text" id="register-name" placeholder="Name" required />
          <input type="email" id="register-email" placeholder="Email" required />
          <input type="password" id="register-password" placeholder="Password" required />
          <button type="submit">Register</button>
        </form>

        <h1>Login</h1>
        <form id="login-form">
          <input type="email" id="login-email" placeholder="Email" required />
          <input type="password" id="login-password" placeholder="Password" required />
          <button type="submit">Login</button>
        </form>

        <div id="message"></div>

        <script src="app.js"></script>
      </body>
      </html>
  ```
2. Create `app.js` to handle form submissions

---

#### **Slide 9: Activity Step 2 - Handling Form Submissions with Fetch API**
- **Instructions:**
  1. Implement registration form handler in `app.js`:
     ```javascript
     document.getElementById('register-form').addEventListener('submit', async (e) => {
       e.preventDefault();
       const name = document.getElementById('register-name').value;
       const email = document.getElementById('register-email').value;
       const password = document.getElementById('register-password').value;

       try {
         const response = await fetch('http://localhost:3000/auth/register', {
           method: 'POST',
           headers: { 'Content-Type': 'application/json' },
           body: JSON.stringify({ name, email, password })
         });
         const data = await response.json();
         document.getElementById('message').textContent = data.message || data.error;
       } catch (error) {
         console.error('Error:', error);
       }
     });
     ```
---

#### **Slide 9: Activity Step 2.1 - Handling Form Submissions with Fetch API**
  2. Implement login form handler:
     ```javascript
     document.getElementById('login-form').addEventListener('submit', async (e) => {
       e.preventDefault();
       const email = document.getElementById('login-email').value;
       const password = document.getElementById('login-password').value;

       try {
         const response = await fetch('http://localhost:3000/auth/login', {
           method: 'POST',
           headers: { 'Content-Type': 'application/json' },
           body: JSON.stringify({ email, password })
         });
         const data = await response.json();
         if (data.token) {
           localStorage.setItem('token', data.token);
           document.getElementById('message').textContent = 'Login successful!';
         } else {
           document.getElementById('message').textContent = data.error;
         }
       } catch (error) {
         console.error('Error:', error);
       }
     });
     ```

---

#### **Slide 10: Activity Step 3 - Implementing CORS on Backend**
- **Instructions:**
  1. Install `cors` middleware:
     ```bash
     npm install cors --save
     ```
  2. Configure CORS in `server.js`:
     ```javascript
     const cors = require('cors');
     app.use(cors({
       origin: 'http://localhost:5500', // Frontend origin
       methods: ['GET', 'POST', 'PUT', 'DELETE'],
       allowedHeaders: ['Content-Type', 'Authorization']
     }));
     ```
  3. Restart the server and test frontend interactions

---

#### **Slide 11: Activity Step 4 - Displaying API Data in Frontend**
- **Instructions:**
  1. After successful login, fetch user profile:
     ```javascript
     const fetchProfile = async () => {
       const token = localStorage.getItem('token');
       try {
         const response = await fetch('http://localhost:3000/users/1', {
           headers: { 'Authorization': `Bearer ${token}` }
         });
         const user = await response.json();
         document.getElementById('user-name').textContent = user.name;
         document.getElementById('user-email').textContent = user.email;
       } catch (error) {
         console.error('Error fetching profile:', error);
       }
     };

     fetchProfile();
     ```
  2. Update `index.html` to display user data:
     ```html
     <h2>User Profile</h2>
     <p>Name: <span id="user-name"></span></p>
     <p>Email: <span id="user-email"></span></p>
     ```
  3. Run the frontend and observe data fetching

---

#### **Slide 12: Implementing CORS Properly**
- **Common Issues:**
  - **CORS Errors:** Occur when frontend tries to access backend without proper CORS settings
- **Solutions:**
  - Ensure `cors` middleware is correctly configured
  - Allow specific origins, methods, and headers as needed
- **Example: Allow All Origins (for development only)**
  ```javascript
  app.use(cors());
  ```
- **Security Note:** Restrict origins in production for enhanced security

---

#### **Slide 13: Best Practices for API Consumption**
- **Handle Errors Gracefully:**
  - Show user-friendly messages
  - Implement retry mechanisms if necessary
- **Secure Storage of Tokens:**
  - Use `localStorage` or `sessionStorage` with caution
  - Consider HTTP-only cookies for enhanced security
- **Optimize Performance:**
  - Use caching strategies
  - Minimize unnecessary API calls

---

#### **Slide 14: Common Pitfalls and How to Avoid Them**
- **Hardcoding URLs:** Use environment variables or configuration files
- **Ignoring Response Status:** Always check response status before processing data
- **Poor Error Handling:** Provide meaningful feedback to users
- **Security Oversights:** Ensure tokens are securely stored and transmitted

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - RESTful communication principles
  - Using Fetch API for HTTP requests in Vanilla JavaScript
  - Handling CORS to enable cross-origin requests
  - Consuming API data and updating the frontend dynamically
- **Questions:** Open floor for any student queries

---

## **Week 3: Frontend Development and Deployment**

### **Module 11: Advanced JavaScript for Frontend**

---

#### **Slide 1: Title Slide**
- **Title:** Advanced JavaScript for Frontend
- **Subtitle:** Week 3, Module 11
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** DOM manipulation techniques
- **Learn** event handling in JavaScript
- **Implement** form validation on the client side
- **Render** dynamic content based on data changes

---

#### **Slide 3: DOM Manipulation Overview**
- **Definition:** Interacting with and modifying the Document Object Model (DOM) using JavaScript
- **Common Tasks:**
  - Selecting elements
  - Changing content and styles
  - Adding or removing elements
- **Methods:**
  - `document.getElementById()`
  - `document.querySelector()`
  - `element.innerHTML`
  - `element.style`

---

#### **Slide 4: Selecting DOM Elements**
- **By ID:**
  ```javascript
  const element = document.getElementById('element-id');
  ```
- **By Class:**
  ```javascript
  const elements = document.getElementsByClassName('class-name');
  ```
- **By Selector:**
  ```javascript
  const element = document.querySelector('.class-name');
  const elements = document.querySelectorAll('div > p');
  ```

---

#### **Slide 5: Modifying DOM Elements**
- **Changing Text Content:**
  ```javascript
  document.getElementById('user-name').textContent = 'Alice';
  ```
- **Changing HTML Content:**
  ```javascript
  document.getElementById('content').innerHTML = '<p>New Content</p>';
  ```
- **Changing Styles:**
  ```javascript
  const button = document.getElementById('submit-btn');
  button.style.backgroundColor = 'blue';
  ```

---

#### **Slide 6: Adding and Removing Elements**
- **Creating Elements:**
  ```javascript
  const newDiv = document.createElement('div');
  newDiv.textContent = 'Hello World';
  document.body.appendChild(newDiv);
  ```
- **Removing Elements:**
  ```javascript
  const element = document.getElementById('remove-me');
  element.parentNode.removeChild(element);
  ```

---

#### **Slide 7: Event Handling in JavaScript**
- **Definition:** Responding to user interactions like clicks, form submissions, and key presses
- **Event Listeners:**
  ```javascript
  const button = document.getElementById('my-button');
  button.addEventListener('click', () => {
    alert('Button clicked!');
  });
  ```
- **Common Events:**
  - `click`
  - `submit`
  - `input`
  - `mouseover`

---

#### **Slide 8: Form Validation on the Client Side**
- **Importance:** Enhance user experience by providing immediate feedback
- **Techniques:**
  - Checking for empty fields
  - Validating email format
  - Ensuring password strength
- **Example:**
  ```javascript
  const form = document.getElementById('register-form');

  form.addEventListener('submit', (e) => {
    const email = document.getElementById('register-email').value;
    const password = document.getElementById('register-password').value;
    let messages = [];

    if (email === '' || password === '') {
      messages.push('All fields are required');
    }

    if (password.length < 6) {
      messages.push('Password must be at least 6 characters');
    }

    if (messages.length > 0) {
      e.preventDefault();
      document.getElementById('message').textContent = messages.join(', ');
    }
  });
  ```

---

#### **Slide 9: Rendering Dynamic Content**
- **Definition:** Updating the UI based on data changes or user interactions
- **Techniques:**
  - Looping through data to create elements
  - Using conditional statements to display content
- **Example: Displaying Transactions**
  ```javascript
  const displayTransactions = (transactions) => {
    const transactionsList = document.getElementById('transactions-list');
    transactionsList.innerHTML = '';

    transactions.forEach(transaction => {
      const li = document.createElement('li');
      li.textContent = `${transaction.type} - $${transaction.amount} - ${transaction.description}`;
      transactionsList.appendChild(li);
    });
  };
  ```

---

#### **Slide 10: Hands-On Activity Overview**
- **Tasks:**
  1. Build interactive forms for the Financial application
  2. Implement client-side validation
  3. Render fetched data dynamically using DOM manipulation

---

#### **Slide 11: Activity Step 1 - Building Interactive Forms**
- **Instructions:**
  1. Update `index.html` to include forms for managing accounts and transactions
     ```html
     <h2>Create Account</h2>
     <form id="account-form">
       <input type="text" id="account-type" placeholder="Account Type" required />
       <input type="number" id="account-balance" placeholder="Initial Balance" required />
       <button type="submit">Create Account</button>
     </form>

     <h2>Record Transaction</h2>
     <form id="transaction-form">
       <select id="transaction-type" required>
         <option value="">Select Type</option>
         <option value="credit">Credit</option>
         <option value="debit">Debit</option>
       </select>
       <input type="number" id="transaction-amount" placeholder="Amount" required />
       <input type="text" id="transaction-description" placeholder="Description" />
       <button type="submit">Record Transaction</button>
     </form>
     ```
  2. Create corresponding handlers in `app.js`

---

#### **Slide 12: Activity Step 2 - Implementing Client-Side Validation**
- **Instructions:**
  1. Add validation to `account-form`:
     ```javascript
     document.getElementById('account-form').addEventListener('submit', (e) => {
       const accountType = document.getElementById('account-type').value;
       const balance = document.getElementById('account-balance').value;
       let messages = [];

       if (accountType === '' || balance === '') {
         messages.push('All fields are required');
       }

       if (balance < 0) {
         messages.push('Balance cannot be negative');
       }

       if (messages.length > 0) {
         e.preventDefault();
         document.getElementById('message').textContent = messages.join(', ');
       }
     });
     ```
  2. Similarly, add validation to `transaction-form`

---

#### **Slide 13: Activity Step 3 - Rendering Fetched Data**
- **Instructions:**
  1. Fetch and display user accounts and transactions after login
     ```javascript
     const fetchAccounts = async () => {
       const token = localStorage.getItem('token');
       try {
         const response = await fetch('http://localhost:3000/accounts', {
           headers: { 'Authorization': `Bearer ${token}` }
         });
         const accounts = await response.json();
         displayAccounts(accounts);
       } catch (error) {
         console.error('Error fetching accounts:', error);
       }
     };

     const displayAccounts = (accounts) => {
       const accountsList = document.getElementById('accounts-list');
       accountsList.innerHTML = '';

       accounts.forEach(account => {
         const li = document.createElement('li');
         li.textContent = `${account.accountType} - $${account.balance}`;
         accountsList.appendChild(li);
       });
     };

     fetchAccounts();
     ```
  2. Update `index.html` to include `accounts-list` and `transactions-list` elements

---

#### **Slide 14: Best Practices for Frontend Development**
- **Separation of Concerns:**
  - Keep HTML, CSS, and JavaScript separate
- **Modular Code:**
  - Break down JavaScript into reusable functions and modules
- **Responsive Design:**
  - Ensure UI works well on various devices and screen sizes
- **Accessibility:**
  - Make the application accessible to all users (use semantic HTML, ARIA labels)

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Advanced DOM manipulation techniques
  - Effective event handling in JavaScript
  - Implementing client-side form validation
  - Rendering dynamic content based on API data
- **Questions:** Open floor for any student queries

---

### **Module 12: Managing State and Data in the Frontend**

---

#### **Slide 1: Title Slide**
- **Title:** Managing State and Data in the Frontend
- **Subtitle:** Week 3, Module 12
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** state management concepts in frontend applications
- **Learn** to use Local Storage and Session Storage
- **Handle** asynchronous data fetching and state updates
- **Update** the UI based on data changes

---

#### **Slide 3: Understanding State Management**
- **Definition:** Managing data that determines the behavior and rendering of the application
- **Importance:**
  - Keeps UI consistent with underlying data
  - Facilitates data sharing across different parts of the application
- **State Types:**
  - **Local State:** Specific to a component or module
  - **Global State:** Shared across multiple components or modules

---

#### **Slide 4: Using Local Storage and Session Storage**
- **Local Storage:**
  - Stores data with no expiration date
  - Accessible across sessions
  - Syntax:
    ```javascript
    localStorage.setItem('key', 'value');
    const value = localStorage.getItem('key');
    ```
- **Session Storage:**
  - Stores data for the duration of the page session
  - Data is cleared when the page session ends
  - Syntax:
    ```javascript
    sessionStorage.setItem('key', 'value');
    const value = sessionStorage.getItem('key');
    ```
- **Use Cases:**
  - **Local Storage:** Persisting user preferences, tokens
  - **Session Storage:** Temporary data during a session

---

#### **Slide 5: Handling Asynchronous Data Fetching**
- **Challenges:**
  - Ensuring data is loaded before rendering
  - Managing loading states and errors
- **Techniques:**
  - Use `async/await` for cleaner asynchronous code
  - Implement loading indicators in the UI
- **Example:**
  ```javascript
  const fetchData = async () => {
    document.getElementById('loader').style.display = 'block';
    try {
      const response = await fetch('http://localhost:3000/data');
      const data = await response.json();
      renderData(data);
    } catch (error) {
      console.error('Error fetching data:', error);
    } finally {
      document.getElementById('loader').style.display = 'none';
    }
  };
  ```

---

#### **Slide 6: Updating the UI Based on Data Changes**
- **Techniques:**
  - Re-render specific parts of the UI when data changes
  - Use event listeners to trigger UI updates
- **Example: Adding a New Transaction**
  ```javascript
  const addTransaction = (transaction) => {
    const transactionsList = document.getElementById('transactions-list');
    const li = document.createElement('li');
    li.textContent = `${transaction.type} - $${transaction.amount} - ${transaction.description}`;
    transactionsList.appendChild(li);
  };
  ```
- **State Synchronization:**
  - Ensure frontend state reflects backend data
  - Update local storage or state variables accordingly

---

#### **Slide 7: Hands-On Activity Overview**
- **Tasks:**
  1. Implement state management for user sessions
  2. Store and retrieve JWT tokens using Local Storage
  3. Manage application state to show/hide UI elements based on authentication
  4. Handle session persistence across page reloads
  5. Implement token expiration and logout functionality

---

#### **Slide 8: Activity Step 1 - Storing JWT Tokens in Local Storage**
- **Instructions:**
  1. After successful login, store JWT token:
     ```javascript
     if (data.token) {
       localStorage.setItem('token', data.token);
       // Update UI to show authenticated state
     }
     ```
  2. Retrieve token when needed:
     ```javascript
     const token = localStorage.getItem('token');
     ```

---

#### **Slide 9: Activity Step 2 - Managing UI Based on Authentication**
- **Instructions:**
  1. Check for token on page load and update UI:
     ```javascript
     window.addEventListener('load', () => {
       const token = localStorage.getItem('token');
       if (token) {
         document.getElementById('login-form').style.display = 'none';
         document.getElementById('dashboard').style.display = 'block';
         fetchProfile();
       } else {
         document.getElementById('login-form').style.display = 'block';
         document.getElementById('dashboard').style.display = 'none';
       }
     });
     ```
  2. Implement logout functionality:
     ```javascript
     document.getElementById('logout-btn').addEventListener('click', () => {
       localStorage.removeItem('token');
       location.reload();
     });
     ```

---

#### **Slide 10: Activity Step 3 - Implementing Session Persistence**
- **Instructions:**
  1. Ensure that upon page reload, the application checks for the token and maintains the authenticated state
  2. Automatically fetch and display user data if token exists
  3. Example:
     ```javascript
     const fetchProfile = async () => {
       const token = localStorage.getItem('token');
       if (!token) return;

       try {
         const response = await fetch('http://localhost:3000/users/1', {
           headers: { 'Authorization': `Bearer ${token}` }
         });
         const user = await response.json();
         document.getElementById('user-name').textContent = user.name;
         document.getElementById('user-email').textContent = user.email;
       } catch (error) {
         console.error('Error fetching profile:', error);
       }
     };
     ```

---

#### **Slide 11: Activity Step 4 - Handling Token Expiration and Logout**
- **Instructions:**
  1. Set token expiration during JWT creation (e.g., 1 hour)
  2. Check token validity before making API requests
  3. Redirect to login if token is expired or invalid
  4. Example Middleware:
     ```javascript
     const authenticateToken = (req, res, next) => {
       const authHeader = req.headers['authorization'];
       const token = authHeader && authHeader.split(' ')[1];

       if (token == null) return res.status(401).json({ error: 'No token provided' });

       jwt.verify(token, 'your_jwt_secret', (err, user) => {
         if (err) return res.status(403).json({ error: 'Invalid or expired token' });
         req.user = user;
         next();
       });
     };
     ```
  5. Implement automatic logout in frontend upon token expiration
     ```javascript
     // Example: Check token expiration
     const checkTokenExpiry = () => {
       const token = localStorage.getItem('token');
       if (!token) return;

       const payload = JSON.parse(atob(token.split('.')[1]));
       const expiry = payload.exp * 1000;
       const now = Date.now();

       if (now > expiry) {
         localStorage.removeItem('token');
         location.reload();
       }
     };

     setInterval(checkTokenExpiry, 60000); // Check every minute
     ```

---

#### **Slide 12: Best Practices for State Management**
- **Centralize State Management:**
  - Use a single source of truth for application state
- **Keep State Minimal:**
  - Only store necessary data
- **Immutable State Updates:**
  - Avoid directly modifying state; use functions to return new state
- **Consistent Data Flow:**
  - Ensure predictable state transitions

---

#### **Slide 13: Common Pitfalls and How to Avoid Them**
- **Overusing Local Storage:**
  - Avoid storing sensitive data in Local Storage
- **State Synchronization Issues:**
  - Ensure frontend state accurately reflects backend data
- **Ignoring Token Expiration:**
  - Always handle token validity and refresh mechanisms
- **Complex State Logic:**
  - Keep state management simple; consider using state management libraries for larger applications

---

#### **Slide 14: Future Considerations**
- **Advanced State Management:**
  - Explore state management libraries like Redux or MobX
- **Token Refresh Mechanisms:**
  - Implement refresh tokens for seamless user experience
- **Enhanced Security:**
  - Use HTTP-only cookies for storing tokens to prevent XSS attacks

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Concepts of state management in frontend applications
  - Using Local Storage and Session Storage for data persistence
  - Managing application state to reflect authentication status
  - Handling token expiration and implementing secure logout
- **Questions:** Open floor for any student queries

---

### **Module 13: Automated Tasks with npm Scripts**

---

#### **Slide 1: Title Slide**
- **Title:** Automated Tasks with npm Scripts
- **Subtitle:** Week 3, Module 13
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the purpose of automating development tasks
- **Learn** to create and manage npm scripts for build processes
- **Implement** linting and formatting code
- **Run** tests using npm scripts

---

#### **Slide 3: Benefits of Automating Development Tasks**
- **Efficiency:** Saves time by automating repetitive tasks
- **Consistency:** Ensures uniform execution of tasks across environments
- **Error Reduction:** Minimizes human errors in task execution
- **Streamlined Workflow:** Simplifies complex processes

---

#### **Slide 4: Common Automated Tasks**
- **Build Processes:** Transpile, bundle, and minify code
- **Linting:** Enforce code style and quality
- **Testing:** Run automated tests
- **Deployment:** Automate deployment steps
- **Watch Tasks:** Monitor file changes and trigger actions

---

#### **Slide 5: Using npm Scripts for Automation**
- **Definition:** Custom commands defined in `package.json` under the `scripts` section
- **Running Scripts:**
  - `npm run <script_name>`
  - Predefined scripts: `start`, `test`, `build`
- **Example:**
  ```json
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "lint": "eslint .",
    "test": "jest"
  }
  ```

---

#### **Slide 6: Setting Up ESLint for Linting**
- **Installation:**
  ```bash
  npm install eslint --save-dev
  ```
- **Initialization:**
  ```bash
  npx eslint --init
  ```
  - Choose appropriate options (e.g., style guide, environment)
- **Configuration:**
  - Generates `.eslintrc.json` with rules and settings

---

#### **Slide 7: Configuring ESLint**
- **Example `.eslintrc.json`:**
  ```json
  {
    "env": {
      "browser": true,
      "es2021": true,
      "node": true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
      "ecmaVersion": 12,
      "sourceType": "module"
    },
    "rules": {
      "indent": ["error", 2],
      "linebreak-style": ["error", "unix"],
      "quotes": ["error", "single"],
      "semi": ["error", "always"]
    }
  }
  ```
- **Running ESLint:**
  ```bash
  npm run lint
  ```

---

#### **Slide 8: Implementing Testing with Jest**
- **Introduction to Jest:**
  - JavaScript testing framework
  - Supports unit and integration testing
- **Installation:**
  ```bash
  npm install jest --save-dev
  ```
- **Configuration:**
  - Add `test` script in `package.json`:
    ```json
    "scripts": {
      "test": "jest"
    }
    ```
- **Example Test:**
  ```javascript
  // tests/user.test.js
  const { User } = require('../models');

  test('User creation', async () => {
    const user = await User.create({
      name: 'Test User',
      email: 'test@example.com',
      password: 'password123'
    });
    expect(user.name).toBe('Test User');
    expect(user.email).toBe('test@example.com');
  });
  ```

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Set up ESLint for code linting
  2. Create custom npm scripts for linting and testing
  3. Implement automated tests using Jest
  4. Run and verify automated tasks

---

#### **Slide 10: Activity Step 1 - Setting Up ESLint**
- **Instructions:**
  1. Install ESLint:
     ```bash
     npm install eslint --save-dev
     ```
  2. Initialize ESLint:
     ```bash
     npx eslint --init
     ```
  3. Follow prompts to configure ESLint based on project needs
  4. Add lint script to `package.json`:
     ```json
     "scripts": {
       "lint": "eslint ."
     }
     ```

---

#### **Slide 11: Activity Step 2 - Creating Custom npm Scripts**
- **Instructions:**
  1. Update `package.json` with scripts:
     ```json
     "scripts": {
       "start": "node server.js",
       "dev": "nodemon server.js",
       "lint": "eslint .",
       "test": "jest"
     }
     ```
  2. Add additional scripts if necessary (e.g., `build`, `precommit`)
  3. Demonstrate running scripts:
     - `npm run lint`
     - `npm run test`

---

#### **Slide 12: Activity Step 3 - Implementing Automated Tests**
- **Instructions:**
  1. Install Jest:
     ```bash
     npm install jest --save-dev
     ```
  2. Create test directory: `mkdir tests`
  3. Create test files (e.g., `tests/user.test.js`)
  4. Write sample tests for models and routes
  5. Run tests: `npm run test`
  6. Observe test results and fix any issues

---

#### **Slide 13: Activity Step 4 - Running and Verifying Automated Tasks**
- **Instructions:**
  1. Run linting:
     ```bash
     npm run lint
     ```
  2. Fix any linting errors based on ESLint feedback
  3. Run tests:
     ```bash
     npm run test
     ```
  4. Ensure all tests pass successfully
  5. Commit changes with proper messages

---

#### **Slide 14: Best Practices for Automation with npm Scripts**
- **Maintain Clear Scripts:**
  - Use descriptive names for scripts
- **Leverage Pre and Post Hooks:**
  - Example: `precommit` to lint before committing
- **Avoid Overcomplicating Scripts:**
  - Keep scripts focused and manageable
- **Document Scripts:**
  - Explain what each script does in `README.md`

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Automating development tasks with npm scripts
  - Setting up and configuring ESLint for code quality
  - Implementing testing with Jest
  - Running and verifying automated scripts to enhance workflow
- **Questions:** Open floor for any student queries

---

### **Module 14: Basic Administration and Maintenance**

---

#### **Slide 1: Title Slide**
- **Title:** Basic Administration and Maintenance
- **Subtitle:** Week 3, Module 14
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** dependency management and updates
- **Learn** to monitor application performance
- **Implement** logging and debugging strategies
- **Develop** backup and restore strategies for MySQL

---

#### **Slide 3: Managing Dependencies and Updates**
- **Importance:**
  - Keep dependencies up-to-date for security and performance
- **Commands:**
  - **Check for outdated packages:** `npm outdated`
  - **Update all packages:** `npm update`
  - **Update specific package:** `npm install <package_name>@latest`
- **Best Practices:**
  - Regularly check for updates
  - Test application after updating dependencies
  - Use semantic versioning constraints wisely

---

#### **Slide 4: Monitoring Application Performance**
- **Importance:** Ensure application runs efficiently and detect bottlenecks
- **Tools:**
  - **PM2:** Process manager for Node.js applications
  - **New Relic:** Performance monitoring
  - **Log Analysis Tools:** ELK stack (Elasticsearch, Logstash, Kibana)
- **Basic Monitoring with PM2:**
  ```bash
  npm install pm2 -g
  pm2 start server.js --name fintech-app
  pm2 status
  pm2 logs fintech-app
  ```

---

#### **Slide 5: Implementing Logging Mechanisms**
- **Purpose:** Track application behavior, errors, and performance
- **Tools:**
  - **morgan:** HTTP request logger middleware
  - **winston:** Versatile logging library
- **Example with Morgan:**
  ```javascript
  const morgan = require('morgan');
  app.use(morgan('combined'));
  ```
- **Example with Winston:**
  ```javascript
  const winston = require('winston');

  const logger = winston.createLogger({
    level: 'info',
    format: winston.format.json(),
    transports: [
      new winston.transports.File({ filename: 'error.log', level: 'error' }),
      new winston.transports.File({ filename: 'combined.log' }),
    ],
  });

  app.use((req, res, next) => {
    logger.info(`${req.method} ${req.url}`);
    next();
  });
  ```

---

#### **Slide 6: Debugging Node.js Applications**
- **Techniques:**
  - **Console Logging:** Simple but effective
  - **Debugger:** Built-in Node.js debugger or VS Code debugging tools
  - **Error Handling:** Gracefully handle and log errors
- **Using VS Code Debugger:**
  1. Set breakpoints in code
  2. Configure launch settings in `launch.json`
  3. Start debugging session
- **Example:**
  ```javascript
  app.get('/', (req, res) => {
    debugger; // Trigger breakpoint
    res.send('Hello World!');
  });
  ```

---

#### **Slide 7: Developing Backup and Restore Strategies for MySQL**
- **Importance:** Protect against data loss and ensure data recovery
- **Backup Methods:**
  - **mysqldump:** Command-line utility to export databases
  - **Automated Backups:** Schedule regular backups using cron jobs or scripts
- **Example with mysqldump:**
  ```bash
  mysqldump -u root -p fintech_app > fintech_app_backup.sql
  ```
- **Restoring from Backup:**
  ```bash
  mysql -u root -p fintech_app < fintech_app_backup.sql
  ```

---

#### **Slide 8: Hands-On Activity Overview**
- **Tasks:**
  1. Implement logging in the Express application using `morgan` or `winston`
  2. Set up basic performance monitoring with PM2
  3. Create scripts for database backups using `mysqldump`
  4. Implement error logging and debugging mechanisms

---

#### **Slide 9: Activity Step 1 - Implementing Logging with Morgan**
- **Instructions:**
  1. Install `morgan`:
     ```bash
     npm install morgan --save
     ```
  2. Configure `morgan` in `server.js`:
     ```javascript
     const morgan = require('morgan');
     app.use(morgan('dev')); // Use 'combined' for detailed logs
     ```
  3. Run the server and observe request logs in the console

---

#### **Slide 10: Activity Step 2 - Setting Up PM2 for Monitoring**
- **Instructions:**
  1. Install PM2 globally:
     ```bash
     npm install pm2 -g
     ```
  2. Start the application with PM2:
     ```bash
     pm2 start server.js --name fintech-app
     ```
  3. Check application status:
     ```bash
     pm2 status
     ```
  4. View logs:
     ```bash
     pm2 logs fintech-app
     ```

---

#### **Slide 11: Activity Step 3 - Creating Backup Scripts**
- **Instructions:**
  1. Create a backup script `backup.sh`:
     ```bash
     #!/bin/bash
     mysqldump -u root -p'your_password' fintech_app > fintech_app_backup_$(date +%F).sql
     ```
  2. Make the script executable:
     ```bash
     chmod +x backup.sh
     ```
  3. Run the script: `./backup.sh`
  4. Verify backup file is created

---

#### **Slide 12: Activity Step 4 - Implementing Error Logging**
- **Instructions:**
  1. Install `winston`:
     ```bash
     npm install winston --save
     ```
  2. Configure `winston` in `server.js`:
     ```javascript
     const winston = require('winston');

     const logger = winston.createLogger({
       level: 'info',
       format: winston.format.json(),
       transports: [
         new winston.transports.File({ filename: 'error.log', level: 'error' }),
         new winston.transports.File({ filename: 'combined.log' }),
       ],
     });

     app.use((req, res, next) => {
       logger.info(`${req.method} ${req.url}`);
       next();
     });

     app.use((err, req, res, next) => {
       logger.error(err.stack);
       res.status(500).json({ error: 'Internal Server Error' });
     });
     ```
  3. Trigger an error and verify logs are recorded in `error.log`

---

#### **Slide 13: Best Practices for Administration and Maintenance**
- **Regular Backups:** Schedule automated backups and verify their integrity
- **Monitor Logs:** Regularly review logs for errors and unusual activities
- **Update Dependencies:** Keep libraries and frameworks up-to-date
- **Optimize Performance:** Identify and resolve bottlenecks using monitoring tools

---

#### **Slide 14: Common Pitfalls and How to Avoid Them**
- **Neglecting Backups:** Always ensure backups are performed regularly
- **Ignoring Logs:** Regularly monitor logs to detect and fix issues early
- **Unmanaged Dependencies:** Keep track of dependencies to prevent vulnerabilities
- **Poor Error Handling:** Implement comprehensive error handling to maintain application stability

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Managing dependencies and ensuring they are up-to-date
  - Monitoring application performance with PM2
  - Implementing logging mechanisms with `morgan` and `winston`
  - Developing backup and restore strategies for MySQL databases
- **Questions:** Open floor for any student queries

---

### **Module 15: Deployment Basics**

---

#### **Slide 1: Title Slide**
- **Title:** Deployment Basics
- **Subtitle:** Week 3, Module 15
- **Instructor Name & Date**

---

#### **Slide 2: Module Objectives**
- **Understand** the deployment process for Node.js applications
- **Learn** to deploy applications to Heroku
- **Configure** environment variables for production
- **Set Up** continuous deployment with GitHub integration

---

#### **Slide 3: Introduction to Deployment**
- **Definition:** Making your application accessible to users on the internet
- **Stages:**
  1. Development
  2. Testing
  3. Production
- **Considerations:**
  - Performance
  - Security
  - Scalability
  - Reliability

---

#### **Slide 4: Deploying Node.js Applications to Heroku**
- **Why Heroku?**
  - Easy to use platform-as-a-service (PaaS)
  - Supports Node.js out of the box
  - Scalable and reliable
- **Prerequisites:**
  - Heroku account
  - Git repository linked to the project

---

#### **Slide 5: Preparing the Application for Deployment**
- **Steps:**
  1. **Procfile:** Define the command to run the application
     - Create a `Procfile` in the root directory:
       ```
       web: node server.js
       ```
  2. **Environment Variables:** Use `dotenv` for local development and Heroku config vars for production
     - Ensure `.env` is included in `.gitignore`
  3. **Port Configuration:**
     ```javascript
     const port = process.env.PORT || 3000;
     ```

---

#### **Slide 6: Deploying to Heroku**
- **Steps:**
  1. **Login to Heroku:**
     ```bash
     heroku login
     ```
  2. **Create a New Heroku App:**
     ```bash
     heroku create fintech-app
     ```
  3. **Set Environment Variables:**
     ```bash
     heroku config:set JWT_SECRET=your_jwt_secret
     heroku config:set DB_HOST=your_db_host
     heroku config:set DB_USER=your_db_user
     heroku config:set DB_PASSWORD=your_db_password
     heroku config:set DB_NAME=fintech_app
     ```
---

#### **Slide 6.1: Deploying to Heroku**
  4. **Push Code to Heroku:**
     ```bash
     git push heroku main
     ```
  5. **Scale the Dynos:**
     ```bash
     heroku ps:scale web=1
     ```
  6. **Open the App:**
     ```bash
     heroku open
     ```

---

#### **Slide 7: Configuring Environment Variables on Heroku**
- **Steps:**
  1. Use Heroku CLI to set config vars:
     ```bash
     heroku config:set KEY=VALUE
     ```
  2. Alternatively, use Heroku Dashboard:
     - Navigate to your app
     - Go to **Settings** > **Config Vars**
     - Add key-value pairs
- **Security Note:** Never commit sensitive data to the repository

---

#### **Slide 8: Setting Up Continuous Deployment with GitHub**
- **Benefits:**
  - Automated deployments on code changes
  - Streamlined workflow
  - Reduced manual intervention
- **Steps:**
  1. **Link GitHub Repository:**
     - Go to Heroku Dashboard
     - Select your app
     - Navigate to **Deploy** tab
     - Under **Deployment Method**, choose **GitHub**
     - Connect to your GitHub account and select the repository
  2. **Enable Automatic Deploys:**
     - Choose the branch (e.g., `main`) to deploy automatically
  3. **Manual Deploys:**
     - Trigger deployment manually from Heroku Dashboard when needed

---

#### **Slide 9: Hands-On Activity Overview**
- **Tasks:**
  1. Prepare the application for deployment (Procfile, environment variables)
  2. Deploy the Financial application to Heroku
  3. Configure environment variables on Heroku
  4. Set up continuous deployment with GitHub
  5. Verify the deployed application

---

#### **Slide 10: Activity Step 1 - Preparing the Application**
- **Instructions:**
  1. Create a `Procfile` in the project root:
     ```
     web: node server.js
     ```
  2. Update `server.js` to use dynamic port:
     ```javascript
     const port = process.env.PORT || 3000;
     ```
  3. Ensure `.env` is included in `.gitignore`
  4. Commit changes:
     ```bash
     git add Procfile server.js
     git commit -m "Prepare app for Heroku deployment"
     ```

---

#### **Slide 11: Activity Step 2 - Deploying to Heroku**
- **Instructions:**
  1. Login to Heroku:
     ```bash
     heroku login
     ```
  2. Create a Heroku app:
     ```bash
     heroku create fintech-app
     ```
  3. Set environment variables:
     ```bash
     heroku config:set JWT_SECRET=your_jwt_secret
     heroku config:set DB_HOST=your_db_host
     heroku config:set DB_USER=your_db_user
     heroku config:set DB_PASSWORD=your_db_password
     heroku config:set DB_NAME=fintech_app
     ```
---

#### **Slide 11: Activity Step 2 - Deploying to Heroku**
  4. Push to Heroku:
     ```bash
     git push heroku main
     ```
  5. Scale the dynos:
     ```bash
     heroku ps:scale web=1
     ```
  6. Open the deployed app:
     ```bash
     heroku open
     ```

---

#### **Slide 12: Activity Step 3 - Configuring Environment Variables**
- **Instructions:**
  1. Access Heroku Dashboard
  2. Select the deployed app
  3. Navigate to **Settings** > **Config Vars**
  4. Add necessary variables (e.g., `JWT_SECRET`, `DB_HOST`)
  5. Ensure the backend uses these variables securely

---

#### **Slide 13: Activity Step 4 - Setting Up Continuous Deployment**
- **Instructions:**
  1. In Heroku Dashboard, go to **Deploy** tab
  2. Under **Deployment Method**, select **GitHub**
  3. Connect to your GitHub repository
  4. Enable **Automatic Deploys** for the `main` branch
  5. Push a commit to GitHub and observe automatic deployment

---

#### **Slide 14: Best Practices for Deployment**
- **Use Environment Variables:** Keep sensitive data out of the codebase
- **Monitor Application Performance:** Use monitoring tools to track performance and errors
- **Automate Deployments:** Reduce manual steps and potential errors
- **Test Before Deploying:** Ensure all features work correctly in the production environment
- **Rollback Strategies:** Have a plan to revert to previous versions if issues arise

---

#### **Slide 15: Summary and Q&A**
- **Recap:**
  - Preparing the application for deployment with Procfile and environment variables
  - Deploying to Heroku and configuring environment variables
  - Setting up continuous deployment with GitHub integration
  - Best practices for deploying and maintaining applications in production
- **Questions:** Open floor for any student queries

---

## **Final Project: Financial Application for FinTech**

---

### **Project Overview**

---

#### **Slide 1: Title Slide**
- **Title:** Final Project: Financial Application for FinTech
- **Subtitle:** Course Capstone
- **Instructor Name & Date**

---

#### **Slide 2: Project Objectives**
- **Apply** full stack web development skills learned throughout the course
- **Develop** a comprehensive Financial application with user authentication, account management, transaction tracking, and data visualization
- **Demonstrate** competencies in data modeling, application routing, npm package management, and deployment

---

#### **Slide 3: Project Features**
- **User Authentication:**
  - Secure registration and login using JWT
- **Account Management:**
  - CRUD operations for financial accounts
- **Transaction Tracking:**
  - Record and monitor financial transactions
- **Data Visualization:**
  - Display financial summaries using charts and tables
- **Responsive UI:**
  - User-friendly frontend built with Vanilla JavaScript
