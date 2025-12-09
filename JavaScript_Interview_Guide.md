# 🚀 Complete JavaScript Interview Preparation & Reference Guide

> **Created for**: Interview Preparation, Quick Revision, and Deep Understanding  
> **Last Updated**: December 2025  
> **Author's Note**: This guide covers everything from basics to advanced ES6+ features with real-world examples

---

## 📑 Table of Contents
1. [JavaScript Introduction](#1-javascript-introduction)
2. [Role of JavaScript in Web Development](#2-role-of-javascript-in-web-development)
3. [Why JavaScript is Popular](#3-why-javascript-is-popular)
4. [Where Does JavaScript Run](#4-where-does-javascript-run)
5. [JavaScript Features](#5-javascript-features)
6. [How to Add JavaScript](#6-how-to-add-javascript)
7. [Output Methods](#7-output-methods)
8. [Variables](#8-variables)
9. [Operators and Expressions](#9-operators-and-expressions)
10. [Type Conversion](#10-type-conversion)
11. [Control Statements](#11-control-statements)
12. [Loops](#12-loops)
13. [Functions](#13-functions)
14. [Arrays](#14-arrays)
15. [Powerful Array Functions](#15-powerful-array-functions)
16. [Objects in JavaScript](#16-objects-in-javascript)
17. [DOM Manipulation](#17-dom-manipulation)
18. [ES6 Features](#18-es6-features)

---

## 1. JavaScript Introduction

### 📌 What is JavaScript?
JavaScript is a **high-level, interpreted programming language** that makes web pages interactive and dynamic. It's one of the core technologies of web development alongside HTML and CSS.

### 📜 History
- **Created**: 1995
- **Creator**: Brendan Eich (at Netscape)
- **Initial Name**: Mocha → LiveScript → JavaScript
- **Time Taken**: Created in just 10 days!
- **Standardization**: ECMAScript (ES) specification

### 🎯 Interactive Features JavaScript Powers
```javascript
// Button interactions
document.getElementById('myBtn').addEventListener('click', function() {
    alert('Button clicked!');
});

// Animations
element.style.transform = 'translateX(100px)';

// Form validation
function validateEmail(email) {
    return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
}

// Games - Simple number guessing
let randomNum = Math.floor(Math.random() * 100) + 1;
```

### 🌐 Modern JavaScript Usage

#### Frontend Development
```javascript
// React Component Example
function Welcome() {
    return <h1>Hello, World!</h1>;
}
```

#### Backend (Node.js)
```javascript
// Express Server
const express = require('express');
const app = express();

app.get('/', (req, res) => {
    res.send('Hello from Node.js!');
});

app.listen(3000);
```

#### Mobile Apps (React Native)
```javascript
import { View, Text } from 'react-native';

export default function App() {
    return (
        <View>
            <Text>Mobile App with JavaScript!</Text>
        </View>
    );
}
```

#### Desktop Apps (Electron)
```javascript
// Electron - Used by VS Code, Slack, Discord
const { app, BrowserWindow } = require('electron');
```

### ❓ Interview Questions

**Q1: What is JavaScript and what are its key characteristics?**  
**A**: JavaScript is a lightweight, interpreted, object-oriented programming language with first-class functions. It's primarily known as a scripting language for web pages but is also used in many non-browser environments like Node.js.

**Q2: Who created JavaScript and why?**  
**A**: Brendan Eich created JavaScript in 1995 at Netscape to add interactivity to web browsers. It was initially created in just 10 days.

**Q3: Is JavaScript the same as Java?**  
**A**: No! Despite similar names, they are completely different languages. Java is a statically-typed, compiled language, while JavaScript is dynamically-typed and interpreted.

**Q4: What can you build with JavaScript today?**  
**A**: Web applications (frontend), servers (Node.js), mobile apps (React Native), desktop apps (Electron), IoT applications, machine learning (TensorFlow.js), and even game development.

**Q5: Why was JavaScript created in just 10 days, and what were the consequences?**  
**A**: Netscape needed a scripting language quickly to compete with Microsoft. The rushed development led to some quirks and inconsistencies that still exist today (like type coercion, `==` vs `===`, etc.).

---

## 2. Role of JavaScript in Web Development

### 🧱 The Trinity of Web Development

```html
<!DOCTYPE html>
<html>
<head>
    <title>Web Development Trinity</title>
    <!-- CSS: Style/Presentation -->
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: blue;
            transition: all 0.3s;
        }
    </style>
</head>
<body>
    <!-- HTML: Structure/Content -->
    <div class="box" id="myBox">Click Me!</div>

    <!-- JavaScript: Behavior/Interactivity -->
    <script>
        document.getElementById('myBox').addEventListener('click', function() {
            this.style.backgroundColor = 'red';
            this.style.transform = 'scale(1.2)';
        });
    </script>
</body>
</html>
```

### 📊 Role Breakdown

| Technology | Role | Analogy |
|------------|------|---------|
| **HTML** | Structure & Content | Skeleton of a house |
| **CSS** | Styling & Layout | Paint, decorations, furniture |
| **JavaScript** | Behavior & Logic | Electrical systems, automation |

### 🎯 Real-World Example

```html
<!-- HTML: Structure -->
<button id="themeToggle">Toggle Theme</button>
<div id="content">
    <h1>Welcome to My Website</h1>
    <p>This is dynamic content.</p>
</div>

<!-- CSS: Style -->
<style>
    .dark-mode {
        background-color: #1a1a1a;
        color: #ffffff;
    }

    .light-mode {
        background-color: #ffffff;
        color: #000000;
    }
</style>

<!-- JavaScript: Behavior -->
<script>
    const toggleBtn = document.getElementById('themeToggle');
    const content = document.getElementById('content');

    toggleBtn.addEventListener('click', () => {
        content.classList.toggle('dark-mode');
        content.classList.toggle('light-mode');
    });
</script>
```

### ❓ Interview Questions

**Q1: Explain the role of HTML, CSS, and JavaScript in web development.**  
**A**: HTML provides the structure (content and semantic meaning), CSS handles presentation (colors, layout, fonts), and JavaScript adds interactivity and dynamic behavior (user interactions, data manipulation, animations).

**Q2: Can you create a website with only HTML and CSS?**  
**A**: Yes, but it will be static without any interactivity. You can't have form validation, dynamic content updates, API calls, or user interactions beyond basic links.

**Q3: What happens if JavaScript is disabled in the browser?**  
**A**: Interactive features stop working - forms won't validate on client-side, dynamic content won't load, SPAs (Single Page Applications) won't work at all. This is why progressive enhancement is important.

**Q4: Can JavaScript replace HTML and CSS?**  
**A**: Technically, frameworks like React can generate HTML via JavaScript, but it's not recommended to replace them entirely. Each has its optimal use case. Separation of concerns makes code more maintainable.

---

## 3. Why JavaScript is Popular

### 🌟 Key Reasons for Popularity

#### 1. Universal Browser Support
```javascript
// Works on ALL modern browsers without any setup
console.log('This runs on Chrome, Firefox, Safari, Edge!');
```

#### 2. Only Language That Runs Natively in Browsers
```javascript
// No compilation needed - write and run immediately
alert('Instant execution!');
```

#### 3. Huge Ecosystem
```bash
# npm (Node Package Manager) has 2+ million packages
npm install express react vue angular
```

#### 4. Full-Stack Development
```javascript
// Frontend (React)
function UserProfile() {
    return <div>User Profile</div>;
}

// Backend (Node.js + Express)
app.get('/api/users', (req, res) => {
    res.json({ users: ['Alice', 'Bob'] });
});

// Database (MongoDB with JavaScript)
db.users.find({ age: { $gt: 18 } });
```

#### 5. Used by Tech Giants

```javascript
// Google - Angular, V8 Engine
// Facebook - React, React Native
// Netflix - Node.js backend
// Amazon - Frontend interactivity
// Microsoft - TypeScript (superset of JS), VS Code
```

### 📈 Statistics (2025)
- **97%+** of all websites use JavaScript
- **Most Popular Language** on GitHub
- **Highest Job Demand** for web developers
- **12+ million** JavaScript developers worldwide

### 🎯 Real Success Stories

```javascript
// PayPal: Moved from Java to Node.js
// Result: 2x faster build times, 35% fewer lines of code

// Netflix: Uses Node.js for backend
// Result: 70% reduction in startup time

// Uber: Built entire web app with JavaScript
// Result: Unified codebase across platforms
```

### ❓ Interview Questions

**Q1: Why is JavaScript so popular despite its quirks?**  
**A**: Because it's the only language that runs natively in browsers, has a massive ecosystem, enables full-stack development, is easy to learn, and has strong community support. The quirks are outweighed by its versatility and ecosystem.

**Q2: What makes JavaScript different from other programming languages?**  
**A**: It's interpreted (no compilation), dynamically typed, runs in browsers, has event-driven architecture, supports multiple programming paradigms (OOP, functional, imperative), and has asynchronous capabilities built-in.

**Q3: Why do companies like Netflix and PayPal choose Node.js?**  
**A**: Node.js offers non-blocking I/O (handles many concurrent connections), uses JavaScript (same language as frontend), has excellent performance for I/O-intensive operations, and allows code sharing between frontend and backend.

**Q4: Is JavaScript still relevant in 2025?**  
**A**: Absolutely! JavaScript continues to evolve (ES2024/ES2025), frameworks are more powerful (Next.js, SvelteKit), and it's expanding to new domains (AI with TensorFlow.js, edge computing with Deno/Bun).

---

## 4. Where Does JavaScript Run

### 💻 Client-Side (Browser)

```javascript
// Runs in the browser - user's computer
console.log('Running in:', window.location.href);

// Access browser APIs
navigator.geolocation.getCurrentPosition((position) => {
    console.log('Latitude:', position.coords.latitude);
    console.log('Longitude:', position.coords.longitude);
});

// Manipulate the DOM
document.body.style.backgroundColor = 'lightblue';

// Store data locally
localStorage.setItem('username', 'JohnDoe');

// Make API calls
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data));
```

**Browser Environment Features:**
- DOM manipulation
- Browser APIs (Geolocation, Camera, Notifications)
- Local Storage / Session Storage
- Cookies
- Canvas / WebGL for graphics

### 🖥️ Server-Side (Node.js)

```javascript
// Runs on the server - your hosting machine
const fs = require('fs');
const http = require('http');

// Read files from server
fs.readFile('data.txt', 'utf8', (err, data) => {
    console.log(data);
});

// Create a web server
const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>Hello from Server!</h1>');
});

server.listen(3000, () => {
    console.log('Server running on port 3000');
});

// Database operations
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/myapp');

// File system operations
const path = require('path');
console.log(__dirname); // Current directory
```

**Node.js Environment Features:**
- File system access
- Database connections
- Server creation
- Command-line tools
- Background jobs

### 📱 Other Environments

```javascript
// React Native (Mobile)
import { Platform } from 'react-native';
console.log(Platform.OS); // 'ios' or 'android'

// Electron (Desktop)
const { app, BrowserWindow } = require('electron');

// IoT (Johnny-Five)
const five = require('johnny-five');
const board = new five.Board();

// Edge Computing (Cloudflare Workers)
addEventListener('fetch', event => {
    event.respondWith(handleRequest(event.request));
});
```

### 🔄 Client vs Server Comparison

| Feature | Client-Side | Server-Side |
|---------|-------------|-------------|
| **Execution** | User's browser | Your server |
| **Access** | DOM, Browser APIs | File system, Databases |
| **Security** | Code is visible | Code is hidden |
| **Performance** | Depends on user device | Depends on server |
| **Common Use** | UI interactions | Business logic, API |

### ❓ Interview Questions

**Q1: What is the difference between client-side and server-side JavaScript?**  
**A**: Client-side runs in the browser, has access to DOM and browser APIs, but limited security. Server-side runs on Node.js, has file system and database access, better security, and handles backend logic.

**Q2: Can you access the DOM in Node.js?**  
**A**: No, DOM doesn't exist in Node.js because there's no browser. However, libraries like jsdom can simulate a DOM environment for testing purposes.

**Q3: What is Node.js?**  
**A**: Node.js is a JavaScript runtime built on Chrome's V8 engine that allows JavaScript to run on the server. It's event-driven, non-blocking, and perfect for I/O-intensive applications.

**Q4: Why can't you use 'window' object in Node.js?**  
**A**: The 'window' object is a browser API representing the browser window. Node.js runs outside the browser, so it uses 'global' object instead.

**Q5: What are the advantages of using JavaScript on both frontend and backend?**  
**A**: Code reusability, single language expertise, easier team collaboration, shared validation logic, faster development, and easier debugging.

---

## 5. JavaScript Features

### 🪶 1. Lightweight

```javascript
// Small file size, minimal overhead
// A simple JavaScript file
console.log('Hello World'); // Just a few bytes!

// Compare to compiled languages - no heavy runtime needed
```

**Why it matters**: Fast loading times, low memory usage, quick execution.

### 🔄 2. Interpreted Language

```javascript
// No compilation step - code runs directly

// ❌ Other languages (Java, C++)
// Write code → Compile → Machine code → Run

// ✅ JavaScript
// Write code → Run (interpreted by JS engine)

console.log('This runs immediately!');
```

**Benefits**: Faster development, easier debugging, instant feedback.

### 🎨 3. Dynamic Language

```javascript
// Variables can change types at runtime
let data = 42;           // Number
console.log(typeof data); // "number"

data = "Hello";          // Now a string
console.log(typeof data); // "string"

data = { name: "John" }; // Now an object
console.log(typeof data); // "object"

data = function() {};    // Now a function
console.log(typeof data); // "function"

// Functions can be created at runtime
const operation = prompt("Enter 'add' or 'multiply':");
const calculate = operation === 'add' 
    ? (a, b) => a + b 
    : (a, b) => a * b;

console.log(calculate(5, 3)); // Dynamic behavior!
```

### ⚡ 4. Event-Driven

```javascript
// Code executes in response to events

// User interactions
document.getElementById('btn').addEventListener('click', function() {
    console.log('Button clicked!');
});

// Mouse events
element.addEventListener('mouseover', handleMouseOver);

// Keyboard events
document.addEventListener('keydown', (e) => {
    if (e.key === 'Enter') {
        console.log('Enter pressed!');
    }
});

// Network events
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log('Data received!'));

// Timer events
setTimeout(() => {
    console.log('Executed after 2 seconds');
}, 2000);

// Custom events
const event = new CustomEvent('userLogin', { 
    detail: { username: 'John' } 
});
document.dispatchEvent(event);

document.addEventListener('userLogin', (e) => {
    console.log(`${e.detail.username} logged in!`);
});
```

### 🌍 5. Cross-Platform

```javascript
// Same code runs everywhere

// ✅ Windows
// ✅ macOS
// ✅ Linux
// ✅ iOS
// ✅ Android
// ✅ All browsers

// Example: This code works universally
const greet = (name) => {
    return `Hello, ${name}!`;
};

console.log(greet('World')); // Works everywhere!
```

### 🔥 Additional Key Features

#### Object-Oriented
```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        return `Hi, I'm ${this.name}`;
    }
}

const john = new Person('John', 30);
console.log(john.greet());
```

#### Functional Programming
```javascript
// First-class functions
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(n => n * 2);
const evens = numbers.filter(n => n % 2 === 0);
const sum = numbers.reduce((acc, n) => acc + n, 0);

console.log(doubled); // [2, 4, 6, 8, 10]
```

#### Asynchronous
```javascript
// Non-blocking code execution
console.log('Start');

setTimeout(() => {
    console.log('Middle (after 1s)');
}, 1000);

console.log('End');

// Output:
// Start
// End
// Middle (after 1s)

// Promises
fetch('https://api.example.com/users')
    .then(res => res.json())
    .then(users => console.log(users))
    .catch(err => console.error(err));

// Async/Await
async function getUsers() {
    try {
        const response = await fetch('https://api.example.com/users');
        const users = await response.json();
        console.log(users);
    } catch (error) {
        console.error(error);
    }
}
```

### ❓ Interview Questions

**Q1: What does it mean that JavaScript is "interpreted"?**  
**A**: JavaScript code is executed line-by-line by a JavaScript engine (like V8) without a separate compilation step. This allows for faster development but can be slower than compiled languages.

**Q2: Explain JavaScript's dynamic typing.**  
**A**: Variables in JavaScript don't have fixed types. The same variable can hold different types of values at different times, and type checking happens at runtime rather than compile-time.

**Q3: What is event-driven programming in JavaScript?**  
**A**: Code execution is triggered by events (user clicks, API responses, timers). JavaScript uses an event loop to handle asynchronous operations and callbacks.

**Q4: Is JavaScript single-threaded? How does it handle multiple operations?**  
**A**: Yes, JavaScript is single-threaded, but it uses an event loop and callback queue to handle asynchronous operations without blocking the main thread.

**Q5: What are the advantages and disadvantages of dynamic typing?**  
**A**: 
- **Advantages**: Flexible, faster to write, no type declarations needed
- **Disadvantages**: Runtime errors, harder to debug, no compile-time type checking (solved by TypeScript)

---

## 6. How to Add JavaScript

### 1️⃣ Inline JavaScript

```html
<!-- JavaScript directly in HTML attributes -->
<!DOCTYPE html>
<html>
<body>
    <!-- onclick attribute -->
    <button onclick="alert('Hello!')">Click Me</button>

    <!-- Multiple statements with semicolons -->
    <button onclick="console.log('Clicked'); alert('Button pressed');">
        Log and Alert
    </button>

    <!-- Function call -->
    <button onclick="greet('John')">Greet</button>

    <script>
        function greet(name) {
            alert('Hello, ' + name);
        }
    </script>
</body>
</html>
```

**❌ Disadvantages:**
- Hard to maintain
- No code reusability
- Mixes HTML and JavaScript
- Violates separation of concerns
- Difficult to debug

**✅ Use Case**: Very small, one-time interactions only.

### 2️⃣ Internal JavaScript

```html
<!DOCTYPE html>
<html>
<head>
    <title>Internal JavaScript</title>

    <!-- Script in <head> -->
    <script>
        // This runs before body loads
        console.log('Script in head');

        // ⚠️ Won't work - DOM not loaded yet
        // document.getElementById('myBtn').click();
    </script>
</head>
<body>
    <h1>Internal JavaScript Example</h1>
    <button id="myBtn">Click Me</button>
    <p id="demo"></p>

    <!-- Script in <body> - RECOMMENDED -->
    <script>
        // This runs after HTML is loaded
        console.log('Script in body');

        // ✅ Works - elements are available
        document.getElementById('myBtn').addEventListener('click', function() {
            document.getElementById('demo').textContent = 'Button clicked!';
        });

        // Multiple functions
        function add(a, b) {
            return a + b;
        }

        function multiply(a, b) {
            return a * b;
        }

        console.log('5 + 3 =', add(5, 3));
        console.log('5 × 3 =', multiply(5, 3));
    </script>
</body>
</html>
```

**✅ Advantages:**
- Better organization than inline
- Can be used on a single page
- Good for small projects

**❌ Disadvantages:**
- No code reusability across pages
- Makes HTML files large
- Harder to maintain in large projects

### 3️⃣ External JavaScript (✅ RECOMMENDED)

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
    <title>External JavaScript</title>
</head>
<body>
    <h1>External JavaScript Example</h1>
    <button id="calculateBtn">Calculate</button>
    <p id="result"></p>

    <!-- Link external JS file - at bottom of body -->
    <script src="script.js"></script>

    <!-- Multiple external files -->
    <script src="utils.js"></script>
    <script src="app.js"></script>

    <!-- From CDN -->
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
</body>
</html>
```

```javascript
// script.js
console.log('External JavaScript loaded!');

document.getElementById('calculateBtn').addEventListener('click', function() {
    const result = calculateSum(10, 20);
    document.getElementById('result').textContent = `Result: ${result}`;
});

function calculateSum(a, b) {
    return a + b;
}
```

```javascript
// utils.js - Reusable utility functions
const Utils = {
    formatCurrency(amount) {
        return `₹${amount.toFixed(2)}`;
    },

    getCurrentDate() {
        return new Date().toLocaleDateString();
    },

    validateEmail(email) {
        return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
    }
};
```

```javascript
// app.js - Main application logic
console.log('Current Date:', Utils.getCurrentDate());
console.log('Price:', Utils.formatCurrency(1299.99));
```

**✅ Advantages:**
- **Reusability**: Use same file across multiple pages
- **Maintainability**: Easy to update in one place
- **Caching**: Browser caches JS files for faster loading
- **Separation**: Clean separation of HTML and JavaScript
- **Collaboration**: Teams can work on separate files

**❌ Disadvantages:**
- Extra HTTP request (solved by bundlers like Webpack)

### ⚙️ Script Loading Strategies

```html
<!-- 1. Normal - Blocks HTML parsing -->
<script src="script.js"></script>

<!-- 2. Async - Downloads in parallel, executes when ready -->
<script src="script.js" async></script>

<!-- 3. Defer - Downloads in parallel, executes after HTML parsed ✅ BEST -->
<script src="script.js" defer></script>

<!-- 4. Module - ES6 modules (defer by default) -->
<script type="module" src="app.js"></script>
```

**Comparison:**

| Attribute | Download | Execution | Use Case |
|-----------|----------|-----------|----------|
| **None** | Blocks parsing | Immediately | Small scripts, bottom of body |
| **async** | Parallel | When ready (random order) | Analytics, ads |
| **defer** | Parallel | After parsing (in order) | **Main scripts ✅** |
| **module** | Parallel | After parsing | ES6 modules |

### 🎯 Best Practices

```html
<!DOCTYPE html>
<html>
<head>
    <title>Best Practices</title>

    <!-- ✅ Third-party libraries in head with defer -->
    <script src="https://cdn.jsdelivr.net/npm/jquery" defer></script>
</head>
<body>
    <div id="app"></div>

    <!-- ✅ Your scripts at bottom with defer -->
    <script src="js/utils.js" defer></script>
    <script src="js/app.js" defer></script>

    <!-- ✅ Analytics with async (doesn't need to block) -->
    <script src="analytics.js" async></script>
</body>
</html>
```

### ❓ Interview Questions

**Q1: What are the different ways to include JavaScript in HTML?**  
**A**: Three ways - Inline (in HTML attributes), Internal (in <script> tags within HTML), and External (separate .js files linked via src attribute). External is the best practice.

**Q2: Where should you place <script> tags and why?**  
**A**: At the bottom of <body> or in <head> with defer attribute. This ensures HTML is parsed before JavaScript executes, preventing errors and improving page load performance.

**Q3: What's the difference between async and defer attributes?**  
**A**: Both download scripts in parallel, but async executes immediately when ready (can be out of order), while defer waits until HTML parsing is complete and maintains script order.

**Q4: Why is external JavaScript preferred?**  
**A**: Code reusability across pages, better maintainability, browser caching, separation of concerns, and easier collaboration in teams.

**Q5: Can you mix internal and external JavaScript?**  
**A**: Yes, but it's not recommended. It makes code harder to maintain. Choose one approach - preferably external JavaScript.

**Q6: What happens if you reference a DOM element before it's loaded?**  
**A**: You'll get null or undefined, leading to errors. Solution: Place scripts at bottom, use defer, or wrap code in DOMContentLoaded event.

---

## 7. Output Methods

### 1️⃣ console.log() - Developer Tool

```javascript
// Basic logging
console.log('Hello, World!');

// Multiple values
console.log('Name:', 'John', 'Age:', 30);

// Variables
let name = 'Alice';
let age = 25;
console.log('User:', name, age);

// Objects and Arrays
const user = { name: 'Bob', role: 'Admin' };
console.log(user); // Expandable object in console

const numbers = [1, 2, 3, 4, 5];
console.log(numbers);

// Template literals
console.log(`Name: ${name}, Age: ${age}`);

// Different console methods
console.error('This is an error message'); // Red color
console.warn('This is a warning'); // Yellow color
console.info('This is info'); // Blue icon
console.table([
    { name: 'John', age: 30 },
    { name: 'Alice', age: 25 }
]); // Displays as table

// Debugging
console.log('Before calculation');
const result = 10 + 20;
console.log('Result:', result);
console.log('After calculation');

// Grouping logs
console.group('User Details');
console.log('Name: John');
console.log('Age: 30');
console.groupEnd();

// Timing
console.time('Loop Time');
for(let i = 0; i < 1000000; i++) {}
console.timeEnd('Loop Time'); // Logs execution time

// Clear console
console.clear();
```

**✅ Use Cases:**
- Debugging code
- Development and testing
- Tracking variable values
- Performance monitoring
- Error detection

**❌ Not Visible to Users** - Only developers see it in browser DevTools (F12).

### 2️⃣ alert() - Browser Popup

```javascript
// Simple alert
alert('Welcome to our website!');

// With variables
let username = 'John';
alert('Hello, ' + username + '!');

// Template literal
alert(`Hello, ${username}!`);

// Confirmation before action
alert('Your form has been submitted successfully!');

// ⚠️ Blocks code execution until user clicks OK
alert('This appears first');
console.log('This runs after OK is clicked');

// Multi-line alert
alert('Line 1\nLine 2\nLine 3');

// Alert with expressions
alert('Total: ' + (10 + 20)); // "Total: 30"
```

**✅ Use Cases:**
- Important notifications
- Error messages
- Welcome messages
- Form submission confirmations

**❌ Disadvantages:**
- Blocks page interaction
- Outdated UI/UX
- Can't be styled
- Annoying for users if overused

**Modern Alternative:**
```javascript
// Use custom modals or toast notifications instead
function showToast(message) {
    const toast = document.createElement('div');
    toast.className = 'toast';
    toast.textContent = message;
    document.body.appendChild(toast);
    setTimeout(() => toast.remove(), 3000);
}
```

### 3️⃣ document.write() - Write to HTML

```javascript
// Write text
document.write('Hello, World!');

// Write HTML
document.write('<h1>Welcome</h1>');
document.write('<p>This is a paragraph</p>');

// With variables
let name = 'John';
document.write('<h2>Hello, ' + name + '</h2>');

// Using loops
for(let i = 1; i <= 5; i++) {
    document.write('<p>Paragraph ' + i + '</p>');
}

// ⚠️ WARNING: If used after page load, it erases everything!
document.addEventListener('DOMContentLoaded', function() {
    document.write('<h1>This erases the entire page!</h1>');
});

// Table generation example
document.write('<table border="1">');
for(let i = 1; i <= 3; i++) {
    document.write('<tr>');
    for(let j = 1; j <= 3; j++) {
        document.write('<td>Cell ' + i + '-' + j + '</td>');
    }
    document.write('</tr>');
}
document.write('</table>');
```

**✅ Use Cases:**
- Simple testing
- Quick prototypes
- Generating HTML during page load

**❌ Disadvantages:**
- Erases entire page if called after load
- Not recommended in modern development
- Poor performance
- Difficult to maintain

**❌ NEVER use in production!**

### 4️⃣ innerHTML - Modern DOM Manipulation (✅ RECOMMENDED)

```javascript
// Change content of existing element
document.getElementById('demo').innerHTML = 'New content!';

// Add HTML elements
document.getElementById('container').innerHTML = `
    <h2>Welcome</h2>
    <p>This is modern JavaScript!</p>
`;

// Dynamic content
let name = 'Alice';
let age = 25;
document.getElementById('userInfo').innerHTML = `
    <h3>User Profile</h3>
    <p>Name: ${name}</p>
    <p>Age: ${age}</p>
`;

// Lists
const fruits = ['Apple', 'Banana', 'Orange'];
document.getElementById('fruitList').innerHTML = fruits
    .map(fruit => `<li>${fruit}</li>`)
    .join('');

// Tables
const users = [
    { name: 'John', age: 30, role: 'Admin' },
    { name: 'Alice', age: 25, role: 'User' }
];

document.getElementById('userTable').innerHTML = `
    <table>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Role</th>
        </tr>
        ${users.map(user => `
            <tr>
                <td>${user.name}</td>
                <td>${user.age}</td>
                <td>${user.role}</td>
            </tr>
        `).join('')}
    </table>
`;
```

### 5️⃣ textContent - Safe Text Only

```javascript
// Set text (no HTML parsing)
document.getElementById('demo').textContent = 'Hello, World!';

// HTML tags are displayed as text (not rendered)
document.getElementById('demo').textContent = '<h1>This appears as text</h1>';

// Safer than innerHTML (prevents XSS attacks)
let userInput = '<script>alert("Hacked!")</script>';
document.getElementById('output').textContent = userInput; // Safe - displays as text
```

### 📊 Comparison Table

| Method | Visible To | Use In Production | Blocks UI | Can Add HTML |
|--------|-----------|-------------------|-----------|--------------|
| **console.log()** | Developers only | ✅ Yes (debugging) | ❌ No | ❌ No |
| **alert()** | Users | ⚠️ Rarely | ✅ Yes | ❌ No |
| **document.write()** | Users | ❌ Never | ❌ No | ✅ Yes |
| **innerHTML** | Users | ✅ Yes | ❌ No | ✅ Yes |
| **textContent** | Users | ✅ Yes | ❌ No | ❌ No (safe) |

### 🎯 Real-World Example

```javascript
// ❌ Bad Practice
alert('Welcome!');
document.write('<h1>Hello</h1>');

// ✅ Good Practice
console.log('Application started');

// Show welcome message
document.getElementById('welcomeMsg').innerHTML = `
    <div class="alert alert-success">
        <h4>Welcome!</h4>
        <p>Thank you for visiting our site.</p>
    </div>
`;

// Log user action
console.log('User clicked button:', event.target.id);

// Safe user input display
document.getElementById('username').textContent = userInput;
```

### ❓ Interview Questions

**Q1: What's the difference between console.log() and alert()?**  
**A**: console.log() prints to browser's developer console (visible only to developers), while alert() shows a popup dialog to users. console.log() doesn't block code execution, but alert() does.

**Q2: Why is document.write() not recommended?**  
**A**: Because if called after page load, it erases the entire document. It's also bad for performance and difficult to maintain. Use innerHTML or DOM manipulation instead.

**Q3: When would you use innerHTML vs textContent?**  
**A**: Use innerHTML when you need to add HTML elements dynamically. Use textContent when displaying plain text, especially user-generated content, as it's safe from XSS attacks.

**Q4: What is XSS and how does textContent prevent it?**  
**A**: XSS (Cross-Site Scripting) is when malicious scripts are injected into web pages. textContent treats everything as plain text, so even if someone inputs `<script>alert('hack')</script>`, it displays as text rather than executing.

**Q5: Can you use console.log() in production code?**  
**A**: Yes, but excessive logging should be removed or controlled via environment flags. Some developers use console.log for error tracking in production, but sensitive data should never be logged.

---

## 8. Variables

Variables are containers for storing data values. JavaScript has three ways to declare variables: `var`, `let`, and `const`.

### 1️⃣ var (Old Method - Avoid in Modern Code)

```javascript
// Basic declaration
var name = 'John';
var age = 30;
var isStudent = true;

// Can be redeclared (⚠️ Problem!)
var name = 'Alice'; // No error - overwrites previous value
console.log(name); // "Alice"

// Function scoped (not block scoped)
function testVar() {
    var x = 10;
    if (true) {
        var x = 20; // Same variable!
        console.log(x); // 20
    }
    console.log(x); // 20 (changed!)
}

// Hoisting
console.log(hoistedVar); // undefined (not error!)
var hoistedVar = 'I am hoisted';

// Can be used before declaration
age = 25;
var age; // Works but confusing

// Global scope issue
var globalVar = 'Global';
function test() {
    var globalVar = 'Local'; // Different variable
    console.log(globalVar); // "Local"
}
console.log(globalVar); // "Global"
```

**❌ Problems with var:**
- Can be redeclared (causes bugs)
- Function-scoped (not block-scoped)
- Hoisting confusion
- Global namespace pollution

### 2️⃣ let (Modern - Block Scoped) ✅ RECOMMENDED

```javascript
// Basic declaration
let username = 'John';
let age = 30;
let isActive = true;

// Cannot be redeclared in same scope
let username = 'Alice'; // ❌ Error: Identifier 'username' has already been declared

// Can be reassigned
let score = 100;
score = 150; // ✅ OK
score = 200; // ✅ OK

// Block scoped
function testLet() {
    let x = 10;
    if (true) {
        let x = 20; // Different variable (block scoped)
        console.log(x); // 20
    }
    console.log(x); // 10 (unchanged)
}

// Practical block scope example
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 1000);
}
// Output: 0, 1, 2 (correct!)

// Compare with var:
for (var j = 0; j < 3; j++) {
    setTimeout(() => console.log(j), 1000);
}
// Output: 3, 3, 3 (wrong! var is not block scoped)

// Temporal Dead Zone (TDZ)
console.log(myLet); // ❌ Error: Cannot access before initialization
let myLet = 'value';

// Limited to if blocks
if (true) {
    let blockVar = 'Inside block';
    console.log(blockVar); // ✅ Works
}
console.log(blockVar); // ❌ Error: blockVar is not defined

// Commonly used in loops
let fruits = ['Apple', 'Banana', 'Orange'];
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
// console.log(i); // ❌ Error: i is not defined outside loop
```

**✅ Advantages of let:**
- Block-scoped (safer)
- Cannot be redeclared
- No hoisting confusion
- Better for loops

### 3️⃣ const (Constant - Cannot be Reassigned) ✅ RECOMMENDED

```javascript
// Basic declaration - MUST be initialized
const PI = 3.14159;
const MAX_SIZE = 100;
const API_KEY = 'abc123xyz';

// Cannot be reassigned
const name = 'John';
name = 'Alice'; // ❌ Error: Assignment to constant variable

// Must be initialized at declaration
const value; // ❌ Error: Missing initializer
value = 10;

// Block scoped (like let)
if (true) {
    const blockConst = 'Block value';
    console.log(blockConst); // ✅ Works
}
// console.log(blockConst); // ❌ Error

// ⚠️ Objects and Arrays: Reference is constant, but content can change
const user = { name: 'John', age: 30 };
user.age = 31; // ✅ OK - modifying property
user.email = 'john@example.com'; // ✅ OK - adding property
console.log(user); // { name: 'John', age: 31, email: 'john@example.com' }

user = { name: 'Alice' }; // ❌ Error: Assignment to constant variable

// Arrays with const
const numbers = [1, 2, 3];
numbers.push(4); // ✅ OK - modifying array
numbers[0] = 10; // ✅ OK
console.log(numbers); // [10, 2, 3, 4]

numbers = [5, 6, 7]; // ❌ Error: Assignment to constant variable

// Prevent object modification (if needed)
const config = Object.freeze({ 
    apiUrl: 'https://api.example.com',
    timeout: 5000 
});
config.timeout = 10000; // Silently fails (strict mode: error)
console.log(config.timeout); // 5000 (unchanged)

// Real-world usage
const TAX_RATE = 0.18;
const calculateTotal = (amount) => amount + (amount * TAX_RATE);

const users = [
    { id: 1, name: 'John' },
    { id: 2, name: 'Alice' }
];
users.push({ id: 3, name: 'Bob' }); // ✅ OK

const REGEX_EMAIL = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
```

**✅ Use const when:**
- Value shouldn't change
- Configuration values
- Function expressions
- Object/array references
- Default choice (use let only if reassignment needed)

### 🔄 Comparison Table

| Feature | var | let | const |
|---------|-----|-----|-------|
| **Scope** | Function | Block | Block |
| **Redeclaration** | ✅ Allowed | ❌ Error | ❌ Error |
| **Reassignment** | ✅ Allowed | ✅ Allowed | ❌ Error |
| **Hoisting** | Yes (undefined) | TDZ | TDZ |
| **Initialization** | Optional | Optional | Required |
| **Use in Modern Code** | ❌ Avoid | ✅ Yes | ✅ Prefer |

### 🎯 Best Practices

```javascript
// ❌ Bad Practice
var x = 10;
var x = 20; // Redeclared - confusing

// ✅ Good Practice
const MAX_RETRIES = 3; // Values that don't change
let attemptCount = 0; // Values that will change

// Default to const, use let only when needed
const users = []; // Array reference doesn't change
users.push({ name: 'John' }); // But we can modify contents

let currentUser = null; // Will be reassigned
currentUser = users[0];

// Configuration objects
const config = {
    apiUrl: 'https://api.example.com',
    timeout: 5000,
    retries: 3
};

// Loop variables
for (let i = 0; i < 10; i++) {
    // use let for loop variables
}

// Function expressions
const greet = (name) => {
    return `Hello, ${name}!`;
};
```

### 🧪 Variable Naming Rules

```javascript
// ✅ Valid names
let userName = 'John';
let user_name = 'John';
let userName123 = 'John';
let $userName = 'John';
let _userName = 'John';
let TOTAL_AMOUNT = 1000;

// ❌ Invalid names
let 123user = 'John'; // Can't start with number
let user-name = 'John'; // No hyphens
let let = 'value'; // Can't use keywords
let user name = 'John'; // No spaces
let user@name = 'John'; // Only $ and _ allowed

// 📝 Naming Conventions
// camelCase for variables and functions
let firstName = 'John';
let getUserData = () => {};

// PascalCase for classes
class UserProfile {}

// UPPERCASE for constants
const API_KEY = 'abc123';
const MAX_RETRIES = 3;

// Meaningful names
let u = 'John'; // ❌ Bad
let userName = 'John'; // ✅ Good

let x = 25; // ❌ Bad
let userAge = 25; // ✅ Good
```

### ❓ Interview Questions

**Q1: What's the difference between var, let, and const?**  
**A**: var is function-scoped, can be redeclared and reassigned. let is block-scoped, can be reassigned but not redeclared. const is block-scoped, cannot be reassigned or redeclared. Modern code should use let and const only.

**Q2: Can you change a const object's properties?**  
**A**: Yes! const prevents reassignment of the variable, but object properties can be modified. The reference is constant, not the content. Use Object.freeze() to make object immutable.

**Q3: What is hoisting?**  
**A**: Hoisting is JavaScript's behavior of moving declarations to the top of their scope during compilation. var is hoisted and initialized with undefined, while let/const are in a Temporal Dead Zone until initialization.

**Q4: What is block scope?**  
**A**: Block scope means a variable declared inside {} is only accessible within that block. let and const are block-scoped, while var is function-scoped.

**Q5: When should you use let vs const?**  
**A**: Default to const for values that won't be reassigned. Use let only when you need to reassign the variable (like loop counters or values that change).

**Q6: Why is var considered bad practice?**  
**A**: var can be redeclared (causing bugs), is function-scoped (not block-scoped), has confusing hoisting behavior, and can pollute global scope. let and const solve these problems.

## 9. Operators and Expressions

### Overview

Operators are symbols that tell JavaScript to perform specific actions on values (operands), such as addition, comparison, or logical evaluation.
An expression is any valid unit of code that resolves to a value (e.g., `2 + 3`, `a > b`, `user.isActive && user.age > 18`).

***

### Arithmetic Operators

**Operators:** `+`, `-`, `*`, `/`, `%`, `**`

```js
let a = 10;
let b = 3;

console.log(a + b);   // 13
console.log(a - b);   // 7
console.log(a * b);   // 30
console.log(a / b);   // 3.333...
console.log(a % b);   // 1  (remainder)
console.log(a ** 2);  // 100 (exponentiation)
```

**Use cases**

- Calculations in dashboards, billing, carts (subtotal, tax, total).
- Pagination logic (page size, offsets, remainder).
- Game logic (scores, health, positions).

***

### Assignment Operators

**Operators:** `=`, `+=`, `-=`, `*=`, `/=`, `%=`

```js
let x = 10;

x += 5;   // x = x + 5 → 15
x -= 3;   // x = x - 3 → 12
x *= 2;   // x = x * 2 → 24
x /= 4;   // x = x / 4 → 6
x %= 5;   // x = x % 5 → 1
```

**Use cases**

- Updating counters (likes, views, retries).
- Accumulating totals in loops.
- Updating state in games or animations.

***

### Comparison Operators

**Operators:** `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `>=`

```js
console.log(5 == '5');    // true  (only value compared)
console.log(5 === '5');   // false (value + type compared)

console.log(10 != '10');  // false
console.log(10 !== '10'); // true

console.log(3 < 5);       // true
console.log(10 >= 10);    // true
```

**Key point:** Always prefer `===` and `!==` to avoid unexpected type coercion.

**Use cases**

- Conditional logic in `if`, `while`, `for`.
- Validating form inputs (age > 18, password length >= 8).
- Search and filter operations (e.g., `user.role === 'admin'`).

***

### Logical Operators

**Operators:** `&&` (AND), `||` (OR), `!` (NOT)

```js
const isLoggedIn = true;
const isAdmin = false;

console.log(isLoggedIn && isAdmin); // false
console.log(isLoggedIn || isAdmin); // true
console.log(!isAdmin);              // true
```

**Short-circuit behavior**

```js
// AND: stops at first falsy
false && console.log('Will not run');

// OR: stops at first truthy
true || console.log('Will not run');
```

**Use cases**

- Complex conditions: `if (isLoggedIn && user.isVerified && user.role === 'admin')`.
- Providing fallbacks: `const title = user.title || 'Guest';`.
- Safely accessing nested props (older style before optional chaining).

***

### Increment and Decrement

**Operators:** `++`, `--` (prefix and postfix)

```js
let n = 5;

console.log(n++); // 5 (returns old value, then n = 6)
console.log(n);   // 6

console.log(++n); // 7 (increments, then returns 7)

// Similarly for --
let m = 3;
console.log(m--); // 3 (then 2)
console.log(--m); // 1
```

**Use cases**

- Loop counters.
- Stepping through arrays / sequences.
- Simple counters for stats, attempts, retries.

***

### String Concatenation with +

```js
const firstName = 'John';
const lastName = 'Doe';

const fullName = firstName + ' ' + lastName;     // 'John Doe'
const message = 'Total: ' + (10 + 20);           // 'Total: 30'

// Beware: number + string → string
console.log(1 + '2');    // '12'
console.log('1' + 2 + 3); // '123'
console.log(1 + 2 + '3'); // '33'
```

**Use cases**

- Quick string building (though template literals are preferred).
- Logging / debugging messages.

***

### Interview-style Questions (Operators)

1. Why is `===` preferred over `==` in JavaScript?
2. What is the output of `console.log(0 == false, 0 === false)` and why?
3. Explain the difference between prefix and postfix `++`.
4. How does short-circuiting work with `&&` and `||`? Show a real example.
5. What will this print and why: `console.log(1 + '2' + 3)` and `console.log(1 + 2 + '3')`?
6. What is the difference between `a += b` and `a = a + b`? Are they always identical?

***

## 10. Type Conversion

### Explicit Type Conversion

**To string**

```js
String(123);        // '123'
(123).toString();   // '123'
String(true);       // 'true'
String(null);       // 'null'
```

**To number**

```js
Number('42');       // 42
Number('42.5');     // 42.5
Number(true);       // 1
Number(false);      // 0
Number('abc');      // NaN

parseInt('42px');   // 42
parseFloat('3.14'); // 3.14
+'10';              // 10 (unary plus)
```

**To boolean**

```js
Boolean(0);         // false
Boolean('');        // false
Boolean(null);      // false
Boolean(undefined); // false
Boolean(NaN);       // false

Boolean('hello');   // true
Boolean(123);       // true
Boolean([]);        // true
Boolean({});        // true
```


***

### Implicit Type Conversion (Coercion)

```js
'5' * 2;        // 10   ('5' converted to number)
'5' - 2;        // 3
'5' + 2;        // '52' (number converted to string)

1 == '1';       // true
0 == false;     // true
'' == false;    // true
null == undefined; // true
```

**Avoid relying on coercion; use explicit conversion + `===`.**

***

### Interview-style Questions (Type Conversion)

1. What is type coercion in JavaScript?
2. What is the difference between `Number('123')` and `parseInt('123abc')`?
3. Which values are falsy in JavaScript?
4. Why does `[] == false` evaluate to true?
5. How would you safely convert user input from a text field to a number?

***

## 11. Control Statements

### if, else if, else

```js
const age = 20;

if (age >= 18) {
  console.log('Adult');
} else {
  console.log('Minor');
}

if (score >= 90) {
  grade = 'A';
} else if (score >= 75) {
  grade = 'B';
} else {
  grade = 'C';
}
```

**Use cases**

- Form validation (password length, required fields).
- Role-based UI (admin vs user).
- Handling different ranges (pricing tiers, grades).

***

### Nested if

```js
if (user) {
  if (user.isActive) {
    console.log('Active user');
  } else {
    console.log('Inactive user');
  }
} else {
  console.log('No user found');
}
```


***

### switch

```js
const role = 'admin';

switch (role) {
  case 'admin':
    console.log('Full access');
    break;
  case 'editor':
    console.log('Can edit content');
    break;
  case 'viewer':
    console.log('Read-only access');
    break;
  default:
    console.log('No role assigned');
}
```

**Use cases**

- Menu / navigation handling.
- Status handling (PENDING, APPROVED, REJECTED).
- Mapping enums to actions.

***

### Ternary Operator

```js
const age = 18;
const canVote = age >= 18 ? 'Yes' : 'No';

const label = isLoggedIn ? 'Logout' : 'Login';
```

**Use cases**

- Simple inline conditions in JSX/templating.
- Short conditional assignments.

***

### Interview-style Questions (Control Flow)

1. When would you use `switch` instead of multiple `if/else`?
2. What happens if you forget `break` in a `switch` case?
3. When is ternary operator a bad idea (readability)?
4. How would you refactor a deeply nested `if/else` chain?

***

## 12. Loops

### for loop

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

**Use cases**

- Iterating over arrays (indexes required).
- Fixed count iterations (e.g., retry N times).

***

### while loop

```js
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```

**Use cases**

- Unknown iteration count in advance (read until condition).

***

### do...while loop

```js
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);
```

**Use cases**

- Run at least once (menus, first prompt, first API call).

***

### break and continue

```js
// break
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i); // 0..4
}

// continue
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i); // 0,1,3,4
}
```


***

### Nested loops

```js
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(`i=${i}, j=${j}`);
  }
}
```

**Use cases**

- Matrices, tables, calendars.
- Comparing all pairs in an array (O(n²) logic).

***

### Interview-style Questions (Loops)

1. When would you choose `while` over `for`?
2. What is an infinite loop and how to avoid it?
3. Why are nested loops dangerous in large datasets?
4. How could you break out of nested loops cleanly?

## 13. Functions

### What is a Function?

A function is a reusable block of code designed to perform a specific task.
Functions help avoid repetition, improve readability, and make code modular.

***

### Function Declaration

```js
function add(a, b) {
  return a + b;
}

const result = add(2, 3); // 5
```

- Hoisted (you can call it before it is defined in the file).

***

### Function Expression

```js
const multiply = function (a, b) {
  return a * b;
};

console.log(multiply(3, 4)); // 12
```

- Not hoisted in the same way (cannot use before assignment).

***

### Arrow Functions (ES6)

```js
// Basic
const sub = (a, b) => a - b;

// With body
const greet = (name) => {
  return `Hello, ${name}`;
};

// Single parameter (parentheses optional)
const square = n => n * n;
```

- Do not have their own `this`, `arguments`, or `prototype`.
- Great for callbacks and functional style.

***

### Parameters, Arguments, Default Parameters

```js
function greetUser(name = 'Guest') {
  console.log(`Hello, ${name}`);
}

greetUser('John'); // Hello, John
greetUser();       // Hello, Guest
```


***

### Function Scope \& Hoisting

```js
function demo() {
  var x = 10;
  let y = 20;
  console.log(x, y);
}
// x and y not accessible outside demo()

console.log(sum(2, 3)); // 5

function sum(a, b) {
  return a + b;
}
```


***

### Interview Questions (Functions)

1. Difference between function declarations and function expressions?
2. How does hoisting work with functions?
3. What is the difference between regular functions and arrow functions for `this`?
4. What are default parameters and why are they useful?
5. What is a higher-order function?

***

## 14. Arrays

### Creating Arrays

```js
const numbers = [1, 2, 3, 4];
const fruits = new Array('Apple', 'Banana', 'Orange');
```


***

### Accessing \& Modifying Elements

```js
console.log(fruits[0]); // 'Apple'
fruits[1] = 'Mango';
```


***

### Array Length

```js
console.log(fruits.length);
```


***

### push, pop, unshift, shift

```js
const arr = [1, 2, 3];

arr.push(4);   // [1,2,3,4]
arr.pop();     // [1,2,3]

arr.unshift(0); // [0,1,2,3]
arr.shift();    // [1,2,3]
```


***

### indexOf, includes

```js
const colors = ['red', 'green', 'blue'];

colors.indexOf('green'); // 1
colors.includes('black'); // false
```


***

### concat, slice, splice, join

```js
const a = [1, 2];
const b = [3, 4];

const merged = a.concat(b); // [1,2,3,4]

const part = merged.slice(1, 3); // [2,3] (does not mutate)

const removed = merged.splice(1, 2); // removes 2 items from index 1

const text = ['Hello', 'World'].join(' '); // 'Hello World'
```


***

### Iteration: for, for...of

```js
const nums = [10, 20, 30];

// Classic for
for (let i = 0; i < nums.length; i++) {
  console.log(nums[i]);
}

// for...of
for (const n of nums) {
  console.log(n);
}
```


***

### Array of Objects

```js
const users = [
  { id: 1, name: 'John', active: true },
  { id: 2, name: 'Alice', active: false }
];
```


***

### Interview Questions (Arrays)

1. Difference between `slice` and `splice`?
2. How to check if a variable is an array? (`Array.isArray`)
3. How would you remove the last element of an array?
4. How to merge two arrays immutably?

***

## 15. Powerful Array Functions

### map

Transforms each element and returns a new array.

```js
const nums = [1, 2, 3];

const doubled = nums.map(n => n * 2); // [2,4,6]
```


***

### filter

Keeps elements that satisfy a condition.

```js
const users = [
  { name: 'John', active: true },
  { name: 'Alice', active: false }
];

const activeUsers = users.filter(u => u.active);
```


***

### reduce

Reduces array to a single value.

```js
const nums = [1, 2, 3, 4];

const sum = nums.reduce((acc, n) => acc + n, 0); // 10
```


***

### sort

Sorts array (mutates original).

```js
const nums = [10, 2, 5, 1];

nums.sort((a, b) => a - b); // [1,2,5,10]
```


***

### Interview Questions (Array Methods)

1. When to use `map` vs `forEach`?
2. How does `reduce` work (explain accumulator \& initial value)?
3. Why is `sort` tricky with numbers in JS?
4. Are `map`, `filter`, `reduce` immutable?

***

## 16. Objects in JavaScript

### Creating Objects

```js
const user = {
  name: 'John',
  age: 30,
  isAdmin: true
};
```


***

### Accessing Properties

```js
console.log(user.name);      // dot notation
console.log(user['age']);    // bracket notation
```


***

### Updating, Adding, Deleting

```js
user.age = 31;
user.email = 'john@example.com';

delete user.isAdmin;
```


***

### Methods \& this

```js
const person = {
  name: 'Alice',
  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
};
```


***

### Nested Objects, for...in

```js
const company = {
  name: 'ABC',
  address: {
    city: 'Delhi',
    country: 'India'
  }
};

for (const key in company) {
  console.log(key, company[key]);
}
```


***

### Object.keys, values, entries, assign, spread

```js
Object.keys(user);    // ['name', 'age', 'email']
Object.values(user);  // ['John', 31, 'john@example.com']
Object.entries(user); // [['name','John'],...]

const target = { a: 1 };
const source = { b: 2 };
Object.assign(target, source); // {a:1,b:2}

const clone = { ...user };
```


***

### Array of Objects

```js
const products = [
  { id: 1, name: 'Laptop', price: 50000 },
  { id: 2, name: 'Phone', price: 20000 }
];
```


***

### Interview Questions (Objects)

1. Difference between dot and bracket notation?
2. How to clone an object (shallow vs deep copy)?
3. What does `this` refer to inside an object method?
4. Difference between `Object.assign` and spread (`...`)?

***

## 17. DOM Manipulation

### What is DOM?

The Document Object Model (DOM) is a tree representation of the HTML document that JavaScript can read and modify.

***

### Selecting Elements

```js
document.getElementById('title');
document.getElementsByClassName('item');
document.getElementsByTagName('p');

document.querySelector('#title');       // CSS selector
document.querySelectorAll('.item');     // NodeList
```


***

### Changing Content and Attributes

```js
const el = document.getElementById('title');

el.innerHTML = '<span>Hello</span>';
el.textContent = 'Plain Text';

el.setAttribute('data-id', '123');
const id = el.getAttribute('data-id');
```


***

### Changing Styles and Classes

```js
el.style.color = 'red';
el.classList.add('active');
el.classList.remove('hidden');
el.classList.toggle('dark-mode');
```


***

### Creating, Appending, Removing

```js
const li = document.createElement('li');
li.textContent = 'New item';

document.getElementById('list').appendChild(li);

li.remove();
```


***

### Events and addEventListener

```js
const btn = document.getElementById('btn');

btn.addEventListener('click', () => {
  console.log('Button clicked');
});

document.addEventListener('keydown', e => {
  if (e.key === 'Enter') {
    console.log('Enter pressed');
  }
});
```


***

### Interview Questions (DOM)

1. Difference between `innerHTML` and `textContent`?
2. How to efficiently handle events for many list items (event delegation)?
3. What is the DOM tree?
4. How do you dynamically create and insert a new element?

***

## 18. ES6 Features

### let and const

Block-scoped variable declarations that replace `var` in modern code.

***

### Template Literals

```js
const name = 'John';
const message = `Hello, ${name}! Welcome.`;
```


***

### Destructuring

```js
const user = { name: 'Alice', age: 25 };

const { name, age } = user;

const arr = [10, 20, 30];
const [first, second] = arr;
```


***

### Spread and Rest

```js
// Spread
const a = [1, 2];
const b = [3, 4];
const merged = [...a, ...b];

// Rest
function sum(...nums) {
  return nums.reduce((acc, n) => acc + n, 0);
}
```


***

### for...of

```js
for (const n of [1, 2, 3]) {
  console.log(n);
}
```


***

### Classes

```js
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
}

const p = new Person('John');
```


***

### Promises

```js
const fetchData = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve('Done'), 1000);
  });
};

fetchData()
  .then(data => console.log(data))
  .catch(err => console.error(err));
```


***

### Async/Await

```js
async function loadUser() {
  try {
    const res = await fetch('/api/user');
    const user = await res.json();
    console.log(user);
  } catch (e) {
    console.error(e);
  }
}
```


***

### Interview Questions (ES6)

1. Difference between `var`, `let`, and `const`?
2. What problems do template literals solve?
3. Explain destructuring with a real example.
4. What is a Promise and what problem does it solve?
5. Difference between Promises and async/await?

***
