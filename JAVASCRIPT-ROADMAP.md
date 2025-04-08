# 🚀 JavaScript Roadmap – From Zero to Hero

Alright folks! So by now you've done HTML and CSS — that's great 🎉

But HTML & CSS only define structure and style.  
What about interaction? What happens when we click a button, change a form, or move things around dynamically?

That's where JavaScript comes in. JavaScript makes your websites alive and interactive 💡

## 🌟 Why JavaScript Matters in 2025

JavaScript is the backbone of modern web development. In 2025, it's impossible to imagine a frontend developer without JavaScript skills. From creating dynamic websites to building full-stack applications, JavaScript is everywhere.

Consider this:
- **95% of websites** use JavaScript in some way
- JavaScript jobs pay **20-30% more** than HTML/CSS-only positions
- It's the only language that runs directly in browsers
- JavaScript now powers backend (Node.js), mobile apps (React Native), and even desktop applications (Electron)

Let's dive into this roadmap and take your skills from zero to hero! 🚀

---

## 🔍 Quick Glance: JavaScript Roadmap  
✅ Basics → Variables, Functions  
✅ DOM → Events, Manipulation  
✅ BOM → Browser Interactions  
✅ Modern JS → ES6, Promises, async/await  
✅ Projects → To-do app, Form validation  
✅ Practice → GitHub, Hosting, Community  

---

## 📍 1. JavaScript Basics  
Before diving into advanced topics, you need a strong foundation.  

### ✅ What is JavaScript?  
JavaScript is a programming language that allows you to add interactivity to your websites. It runs in the browser and powers everything from animations to complex web apps.

**Real-world example:** Ever noticed how Facebook updates your notifications without refreshing the page? That's JavaScript!

### ✅ How Browsers Run JavaScript  
Browsers have JavaScript engines (like Chrome's V8 or Firefox's SpiderMonkey) that execute your code.

When you load a webpage:
1. Browser downloads the HTML
2. Parses the HTML and creates the DOM
3. Encounters the `<script>` tag
4. Downloads, parses, and executes the JavaScript

### ✅ Linking JavaScript to HTML  
You can add JavaScript to your HTML in three ways:

**1. External JavaScript (Recommended):**
```html
<script src="script.js"></script>
```

**2. Internal JavaScript:**
```html
<script>
  alert("Hello, world!");
</script>
```

**3. Inline JavaScript (Avoid when possible):**
```html
<button onclick="alert('Hello!')">Click me</button>
```

### 📌 Variables & Data Types  
Variables are like containers that store values.

**Variable Declaration:**
```javascript
// Modern way (use these!)
let name = "Ram";       // Can be changed later
const age = 20;         // Cannot be changed

// Old way (avoid)
var school = "ABC";     // Older syntax with scope issues
```

**Data Types:**
```javascript
// Primitive types
let name = "Sita";              // String
let age = 22;                   // Number
let isStudent = true;           // Boolean
let future;                     // Undefined
let nothing = null;             // Null
let uniqueId = Symbol("id");    // Symbol

// Non-primitive types
let marks = [98, 95, 92];       // Array
let student = {                 // Object
  name: "Hari",
  age: 21
};
```

### 📌 Operators  
**Arithmetic:**
```javascript
let sum = 5 + 10;      // Addition: 15
let diff = 10 - 5;     // Subtraction: 5
let product = 5 * 10;  // Multiplication: 50
let quotient = 10 / 5; // Division: 2
let remainder = 10 % 3;// Modulus: 1
```

**Comparison:**
```javascript
5 == "5"    // true (equality, converts types)
5 === "5"   // false (strict equality, checks types)
5 != "5"    // false (inequality)
5 !== "5"   // true (strict inequality)
5 > 3       // true (greater than)
5 >= 5      // true (greater than or equal)
```

**Logical:**
```javascript
true && false  // AND: false
true || false  // OR: true
!true          // NOT: false
```

**Assignment:**
```javascript
let x = 5;
x += 3;        // Same as: x = x + 3 (now x is 8)
x -= 2;        // Same as: x = x - 2 (now x is 6)
x *= 2;        // Same as: x = x * 2 (now x is 12)
```

---

## 📍 2. Control Structures  
Control the flow of your program:

### If...else
```javascript
let marks = 85;

if (marks >= 80) {
  console.log("Distinction");
} else if (marks >= 60) {
  console.log("First Division");
} else {
  console.log("Try harder next time");
}
```

### Switch
```javascript
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week");
    break;
  case "Friday":
    console.log("End of the week");
    break;
  default:
    console.log("Mid-week");
}
```

### Loops

**For Loop:**
```javascript
// Print numbers 1 to 5
for (let i = 1; i <= 5; i++) {
  console.log(i); 
}
```

**While Loop:**
```javascript
// Print numbers 1 to 5
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

**For...of (Iterate Arrays):**
```javascript
const fruits = ["Apple", "Banana", "Mango"];
for (const fruit of fruits) {
  console.log(fruit);
}
```

**For...in (Iterate Object Properties):**
```javascript
const student = {
  name: "Sita",
  age: 20,
  faculty: "BCA"
};

for (const key in student) {
  console.log(key + ": " + student[key]);
}
```

---

## 📍 3. Functions in JavaScript  
Functions are the building blocks of JavaScript. They let you reuse code.

### Function Declaration
```javascript
function greet(name) {
  return "Hello, " + name + "!";
}

console.log(greet("Hari")); // Output: Hello, Hari!
```

### Function Expression
```javascript
const greet = function(name) {
  return "Hello, " + name + "!";
};

console.log(greet("Sita")); // Output: Hello, Sita!
```

### Arrow Functions (ES6)
```javascript
const greet = (name) => {
  return "Hello, " + name + "!";
};

// Shorter syntax for one-line functions
const greetShort = name => "Hello, " + name + "!";

console.log(greetShort("Ram")); // Output: Hello, Ram!
```

### Callback Functions
Functions passed as arguments to other functions.

```javascript
function processInput(input, callback) {
  const processed = input.toUpperCase();
  callback(processed);
}

processInput("hello", function(result) {
  console.log(result); // Output: HELLO
});
```

### IIFE (Immediately Invoked Function Expression)
Functions that run as soon as they are defined.

```javascript
(function() {
  console.log("I run immediately!");
})();
```

### Higher-order Functions
Functions that take other functions as arguments or return functions.

```javascript
function multiplier(factor) {
  return function(number) {
    return number * factor;
  };
}

const doubleIt = multiplier(2);
console.log(doubleIt(5)); // Output: 10
```

---

## 📍 4. Arrays & Objects  

### Arrays
Arrays store ordered collections of data.

```javascript
// Creating arrays
const fruits = ["Apple", "Banana", "Orange"];
const mixedArray = [1, "hello", true, [1, 2]];

// Accessing elements
console.log(fruits[0]); // Output: Apple

// Array length
console.log(fruits.length); // Output: 3
```

#### Common Array Methods

```javascript
const numbers = [1, 2, 3, 4, 5];

// Adding/Removing elements
numbers.push(6);        // Add to end: [1,2,3,4,5,6]
numbers.pop();          // Remove from end: [1,2,3,4,5]
numbers.unshift(0);     // Add to beginning: [0,1,2,3,4,5]
numbers.shift();        // Remove from beginning: [1,2,3,4,5]

// Useful array operations
const doubledNumbers = numbers.map(num => num * 2);    // [2,4,6,8,10]
const evenNumbers = numbers.filter(num => num % 2 === 0); // [2,4]
const sum = numbers.reduce((total, num) => total + num, 0); // 15

// Slicing and splicing
const sliced = numbers.slice(1, 3);  // [2,3] (doesn't modify original)
numbers.splice(1, 2, 'a', 'b');      // Replace elements (modifies original)
```

### Objects
Objects store key-value pairs.

```javascript
// Creating an object
const student = {
  name: "Ram Sharma",
  age: 21,
  faculty: "BCA",
  isActive: true,
  address: {
    city: "Kathmandu",
    country: "Nepal"
  },
  hobbies: ["Coding", "Reading"]
};

// Accessing properties
console.log(student.name);           // Dot notation
console.log(student["faculty"]);     // Bracket notation

// Adding/modifying properties
student.semester = 4;
student.age = 22;

// Object methods
const keys = Object.keys(student);   // Get all keys
const values = Object.values(student); // Get all values
```

### Destructuring (ES6)
Extract values from objects and arrays easily.

```javascript
// Object destructuring
const { name, age } = student;
console.log(name, age); // Output: Ram Sharma 21

// Array destructuring
const [first, second] = fruits;
console.log(first, second); // Output: Apple Banana

// With default values
const { city, zipCode = "44600" } = student.address;
```

### Spread Operator (...)
```javascript
// Copy arrays
const originalArray = [1, 2, 3];
const newArray = [...originalArray, 4, 5]; // [1,2,3,4,5]

// Copy objects
const updatedStudent = { 
  ...student, 
  age: 22, 
  semester: 5 
};
```

---

## 📍 5. Strings & Numbers  

### String Methods
```javascript
const text = "Hello, JavaScript!";

// Properties
console.log(text.length); // 19

// Common methods
console.log(text.toUpperCase()); // "HELLO, JAVASCRIPT!"
console.log(text.toLowerCase()); // "hello, javascript!"
console.log(text.indexOf("Java")); // 7
console.log(text.includes("Script")); // true
console.log(text.startsWith("Hello")); // true
console.log(text.endsWith("!")); // true

// Extracting parts
console.log(text.slice(7, 11)); // "Java"
console.log(text.split(", ")); // ["Hello", "JavaScript!"]

// Template literals (ES6)
const name = "Hari";
const greeting = `Hello, ${name}! Welcome to JS.`;
```

### Number Methods
```javascript
const num = 123.456;

console.log(num.toFixed(2));        // "123.46" (rounds to 2 decimal places)
console.log(parseInt("42.9"));      // 42 (converts string to integer)
console.log(parseFloat("42.9"));    // 42.9 (converts string to float)
console.log(isNaN("hello"));        // true (checks if not a number)

// Math object
console.log(Math.round(num));       // 123 (rounds to nearest integer)
console.log(Math.floor(num));       // 123 (rounds down)
console.log(Math.ceil(num));        // 124 (rounds up)
console.log(Math.random());         // Random number between 0 and 1
console.log(Math.max(5, 10, 15));   // 15
```

---

## 📍 6. DOM Manipulation  
The DOM (Document Object Model) allows JavaScript to interact with HTML elements dynamically.

### Accessing Elements
```javascript
// By ID
const header = document.getElementById("header");

// By Class Name
const items = document.getElementsByClassName("item"); // Returns HTMLCollection

// By Tag Name
const paragraphs = document.getElementsByTagName("p"); // Returns HTMLCollection

// CSS Selectors (Modern and Recommended)
const firstButton = document.querySelector("button"); // First match
const allButtons = document.querySelectorAll("button"); // All matches (NodeList)
const specificElement = document.querySelector("#header .title");
```

### Manipulating Elements
```javascript
// Changing content
element.textContent = "New text"; // Just text, safer
element.innerHTML = "<span>New HTML</span>"; // Can include HTML (be careful!)

// CSS manipulation
element.style.color = "red";
element.style.fontSize = "20px";
element.style.display = "none"; // Hide element

// CSS classes
element.classList.add("active");
element.classList.remove("hidden");
element.classList.toggle("highlight"); // Add if absent, remove if present
element.classList.contains("active"); // Check if class exists

// Attributes
element.setAttribute("src", "image.jpg");
element.getAttribute("href");
element.removeAttribute("disabled");
```

### Creating and Removing Elements
```javascript
// Create element
const newDiv = document.createElement("div");
newDiv.textContent = "I'm a new div!";
newDiv.classList.add("new-element");

// Add to document
document.body.appendChild(newDiv); // Add as last child
parentElement.insertBefore(newDiv, existingChild); // Add before specific element

// Remove element
element.remove(); // Modern way
parentElement.removeChild(childElement); // Old way
```

### Real-world Example: Creating a Dynamic List
```javascript
function addItem() {
  const input = document.getElementById("newItem");
  const list = document.getElementById("itemList");
  
  if(input.value.trim() !== "") {
    // Create new list item
    const li = document.createElement("li");
    li.textContent = input.value;
    
    // Add delete button
    const deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.onclick = function() {
      li.remove();
    };
    
    li.appendChild(deleteBtn);
    list.appendChild(li);
    input.value = ""; // Clear input
  }
}
```

---

## 📍 7. Events in JavaScript  
Events make your website interactive.

### Common Event Types
- **Mouse events:** `click`, `dblclick`, `mouseover`, `mouseout`
- **Keyboard events:** `keydown`, `keyup`, `keypress`
- **Form events:** `submit`, `change`, `focus`, `blur`
- **Document/Window events:** `load`, `resize`, `scroll`

### Event Handlers
Three ways to handle events:

**1. HTML Attribute (avoid):**
```html
<button onclick="alert('Clicked!')">Click Me</button>
```

**2. Property (simple cases):**
```javascript
const button = document.querySelector("button");
button.onclick = function() {
  alert("Button clicked!");
};
```

**3. Event Listeners (best practice):**
```javascript
const button = document.querySelector("button");
button.addEventListener("click", function() {
  alert("Button clicked!");
});

// Multiple listeners for same event
button.addEventListener("click", function() {
  console.log("Another handler");
});
```

### The Event Object
```javascript
button.addEventListener("click", function(event) {
  // Event information
  console.log(event.type); // "click"
  console.log(event.target); // The button element
  
  // Prevent default behavior
  event.preventDefault(); // Stop form submission, link navigation, etc.
  
  // Stop propagation
  event.stopPropagation(); // Prevent event bubbling
});
```

### Event Bubbling & Capturing
```javascript
// Bubbling (default): Inner to outer elements
// Capturing: Outer to inner elements

// Third parameter: useCapture
element.addEventListener("click", handler, true); // Use capturing phase
```

### Example: Form Validation
```javascript
document.getElementById("myForm").addEventListener("submit", function(event) {
  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;
  let valid = true;
  
  // Simple validation
  if (name.trim() === "") {
    document.getElementById("nameError").textContent = "Name is required";
    valid = false;
  }
  
  if (!email.includes("@")) {
    document.getElementById("emailError").textContent = "Invalid email";
    valid = false;
  }
  
  // Prevent submission if invalid
  if (!valid) {
    event.preventDefault();
  }
});
```

---

## 📍 8. BOM (Browser Object Model)  
Interact with the browser window itself.

### The window Object
The `window` object is the global object in browser JavaScript.

```javascript
// Window dimensions
const width = window.innerWidth;
const height = window.innerHeight;

// Dialog boxes
window.alert("Warning message!");
const confirmed = window.confirm("Are you sure?");
const input = window.prompt("Enter your name", "Default value");

// Timing functions
const timeoutId = window.setTimeout(() => {
  console.log("This runs after 2 seconds");
}, 2000);

const intervalId = window.setInterval(() => {
  console.log("This runs every 1 second");
}, 1000);

// Clear timers
window.clearTimeout(timeoutId);
window.clearInterval(intervalId);
```

### Location Object
```javascript
// Current URL information
console.log(window.location.href);    // Full URL
console.log(window.location.hostname); // Domain name
console.log(window.location.pathname); // Path after domain
console.log(window.location.search);   // Query string

// Navigation
window.location.href = "https://example.com"; // Redirect
window.location.reload();                     // Refresh page
```

### History Object
```javascript
window.history.back();      // Go back one page
window.history.forward();   // Go forward one page
window.history.go(-2);      // Go back two pages
```

### Navigator Object
```javascript
// Browser information
console.log(navigator.userAgent);     // Browser ID string
console.log(navigator.language);      // Browser language
console.log(navigator.onLine);        // Online status
console.log(navigator.platform);      // Operating system
```

---

## 📍 9. Error Handling  
Handle errors gracefully to prevent your program from crashing.

### Try...Catch
```javascript
try {
  // Code that might cause an error
  const data = JSON.parse(invalidJson); // This will fail if invalidJson isn't valid
  console.log(data);
} catch (error) {
  // Error handling code
  console.error("Failed to parse JSON:", error.message);
} finally {
  // This always runs, regardless of error
  console.log("Processing complete");
}
```

### Throwing Custom Errors
```javascript
function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero");
  }
  return a / b;
}

try {
  const result = divide(10, 0);
} catch (error) {
  console.error(error.message); // "Cannot divide by zero"
}
```

### Error Types
```javascript
// Common built-in error types
try {
  const num = undefinedVariable; // ReferenceError
  "hello".toUpperCase(1);        // TypeError
  JSON.parse("{bad json}");      // SyntaxError
} catch (error) {
  if (error instanceof ReferenceError) {
    console.log("Reference error occurred");
  } else if (error instanceof TypeError) {
    console.log("Type error occurred");
  }
}
```

---

## 📍 10. Modern JavaScript (ES6+)  
Modern JavaScript features make your code cleaner and more powerful.

### let and const
```javascript
// Block-scoped variables
if (true) {
  var x = 10; // Function scoped
  let y = 20; // Block scoped
  const z = 30; // Block scoped and constant
}
console.log(x); // 10
console.log(y); // ReferenceError: y is not defined
```

### Template Literals
```javascript
const name = "Ram";
const age = 21;

// Old way
console.log("My name is " + name + " and I am " + age + " years old.");

// Template literals
console.log(`My name is ${name} and I am ${age} years old.`);

// Multi-line strings
const html = `
  <div>
    <h1>Hello ${name}</h1>
    <p>Welcome to our site!</p>
  </div>
`;
```

### Arrow Functions
```javascript
// Traditional function
function add(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;

// With one parameter (parentheses optional)
const square = x => x * x;

// With no parameters
const sayHello = () => "Hello!";

// Block body requires explicit return
const multiply = (a, b) => {
  const result = a * b;
  return result;
};
```

### Default Parameters
```javascript
function greet(name = "Guest", greeting = "Hello") {
  return `${greeting}, ${name}!`;
}

console.log(greet()); // "Hello, Guest!"
console.log(greet("Ram")); // "Hello, Ram!"
console.log(greet("Sita", "Namaste")); // "Namaste, Sita!"
```

### Promises
Promises handle asynchronous operations elegantly.

```javascript
// Creating a promise
const fetchData = new Promise((resolve, reject) => {
  // Simulate an API call
  setTimeout(() => {
    const success = true;
    
    if (success) {
      resolve({ id: 1, name: "Ram" });
    } else {
      reject("Error: Could not fetch data");
    }
  }, 2000);
});

// Using a promise
fetchData
  .then(data => {
    console.log("Success:", data);
    return data.id;
  })
  .then(id => {
    console.log("User ID:", id);
  })
  .catch(error => {
    console.error(error);
  })
  .finally(() => {
    console.log("Operation complete");
  });
```

### Async/Await
A cleaner way to work with promises.

```javascript
async function getUserData(userId) {
  try {
    // Wait for the promise to resolve
    const response = await fetch(`https://api.example.com/users/${userId}`);
    
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    
    const data = await response.json();
    return data;
  } catch (error) {
    console.error("Failed to fetch user:", error);
    return null;
  }
}

// Using the async function
async function displayUser() {
  const user = await getUserData(123);
  console.log(user);
}

displayUser();
```

### Modules
Organize your code into separate files.

```javascript
// utils.js
export function formatDate(date) {
  return date.toLocaleDateString();
}

export const PI = 3.14159;

export default class Calculator {
  add(a, b) {
    return a + b;
  }
}

// main.js
import Calculator, { formatDate, PI } from './utils.js';

const calc = new Calculator();
console.log(calc.add(5, 10)); // 15
console.log(formatDate(new Date())); // "6/15/2023"
console.log(PI); // 3.14159
```

---

## 📍 11. JSON (JavaScript Object Notation)  
JSON is a lightweight data format used for storing and exchanging data.

### JSON Syntax
```json
{
  "name": "Ram Sharma",
  "age": 21,
  "isStudent": true,
  "subjects": ["JavaScript", "Python", "Database"],
  "address": {
    "city": "Kathmandu",
    "country": "Nepal"
  }
}
```

### JSON Methods
```javascript
// JavaScript object
const student = {
  name: "Ram",
  age: 21,
  isActive: true
};

// Convert object to JSON string
const jsonString = JSON.stringify(student);
console.log(jsonString); // '{"name":"Ram","age":21,"isActive":true}'

// Parse JSON back to JavaScript object
const parsedObject = JSON.parse(jsonString);
console.log(parsedObject.name); // "Ram"

// Handling errors in JSON parsing
try {
  const invalidJson = '{"name": "Ram", age: 21}'; // Invalid JSON (missing quotes)
  JSON.parse(invalidJson);
} catch (error) {
  console.error("Invalid JSON:", error.message);
}
```

### Working with APIs
```javascript
// Fetching JSON data
async function fetchUsers() {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/users');
    const users = await response.json();
    
    // Now we can work with the JSON data
    users.forEach(user => {
      console.log(user.name, user.email);
    });
    
    return users;
  } catch (error) {
    console.error('Error fetching users:', error);
  }
}

fetchUsers();
```

---

## 📍 12. JavaScript in the Real World  

### Fetch API for AJAX Requests
```javascript
// GET request
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  })
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));

// POST request
fetch('https://api.example.com/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    name: 'Ram',
    email: 'ram@example.com'
  })
})
  .then(response => response.json())
  .then(data => console.log('User created:', data))
  .catch(error => console.error('Error:', error));
```

### Web Storage
```javascript
// LocalStorage (persists even after browser close)
localStorage.setItem('username', 'ram123');
localStorage.setItem('theme', 'dark');

const username = localStorage.getItem('username');
console.log(username); // "ram123"

localStorage.removeItem('theme'); // Remove single item
localStorage.clear(); // Clear all items

// SessionStorage (cleared when page session ends)
sessionStorage.setItem('temporaryData', 'something');
```

### Form Validation Example
```javascript
document.getElementById('registrationForm').addEventListener('submit', function(event) {
  // Prevent form from submitting by default
  event.preventDefault();
  
  // Get form fields
  const username = document.getElementById('username').value;
  const password = document.getElementById('password').value;
  const email = document.getElementById('email').value;
  
  // Validation flags
  let isValid = true;
  
  // Username validation
  if (username.length < 3) {
    document.getElementById('usernameError').textContent = 'Username must be at least 3 characters';
    isValid = false;
  } else {
    document.getElementById('usernameError').textContent = '';
  }
  
  // Password validation
  if (password.length < 8) {
    document.getElementById('passwordError').textContent = 'Password must be at least 8 characters';
    isValid = false;
  } else {
    document.getElementById('passwordError').textContent = '';
  }
  
  // Email validation using regex
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  if (!emailRegex.test(email)) {
    document.getElementById('emailError').textContent = 'Please enter a valid email';
    isValid = false;
  } else {
    document.getElementById('emailError').textContent = '';
  }
  
  // If all validations pass
  if (isValid) {
    // Submit the form
    console.log('Form is valid, submitting...');
    this.submit();
  }
});
```

### Real Project: To-Do List App
```javascript
// HTML structure:
// <input id="taskInput">
// <button id="addTaskBtn">Add Task</button>
// <ul id="taskList"></ul>

document.addEventListener('DOMContentLoaded', function() {
  const taskInput = document.getElementById('taskInput');
  const addTaskBtn = document.getElementById('addTaskBtn');
  const taskList = document.getElementById('taskList');
  
  // Load tasks from localStorage
  loadTasks();
  
  // Add task event
  addTaskBtn.addEventListener('click', function() {
    addTask();
  });
  
  // Enter key also adds task
  taskInput.addEventListener('keypress', function(e) {
    if (e.key === 'Enter') {
      addTask();
    }
  });
  
  function addTask() {
    const taskText = taskInput.value.trim();
    if (taskText === '') return;
    
    // Create task element
    const li = document.createElement('li');
    li.innerHTML = `
      <span class="task-text">${taskText}</span>
      <button class="delete-btn">Delete</button>
      <button class="complete-btn">Complete</button>
    `;
    
    // Add delete functionality
    const deleteBtn = li.querySelector('.delete-btn');
    deleteBtn.addEventListener('click', function() {
      li.remove();
      saveTasks();
    });
    
    // Add complete functionality
    const completeBtn = li.querySelector('.complete-btn');
    completeBtn.addEventListener('click', function() {
      li.querySelector('.task-text').classList.toggle('completed');
      saveTasks();
    });
    
    // Add to list
    taskList.appendChild(li);
    
    // Clear input
    taskInput.value = '';
    
    // Save tasks
    saveTasks();
  }
  
  function saveTasks() {
    const tasks = [];
    document.querySelectorAll('#taskList li').forEach(function(taskEl) {
      const taskText = taskEl.querySelector('.task-text').textContent;
      const isCompleted = taskEl.querySelector('.task-text').classList.contains('completed');
      
      tasks.push({
        text: taskText,
        completed: isCompleted
      });
    });
    
    localStorage.setItem('tasks', JSON.stringify(tasks));
  }
  
  function loadTasks() {
    const savedTasks = localStorage.getItem('tasks');
    if (savedTasks) {
      const tasks = JSON.parse(savedTasks);
      
      tasks.forEach(function(task) {
        const li = document.createElement('li');
        li.innerHTML = `
          <span class="task-text ${task.completed ? 'completed' : ''}">${task.text}</span>
          <button class="delete-btn">Delete</button>
          <button class="complete-btn">Complete</button>
        `;
        
        // Add delete functionality
        const deleteBtn = li.querySelector('.delete-btn');
        deleteBtn.addEventListener('click', function() {
          li.remove();
          saveTasks();
        });
        
        // Add complete functionality
        const completeBtn = li.querySelector('.complete-btn');
        completeBtn.addEventListener('click', function() {
          li.querySelector('.task-text').classList.toggle('completed');
          saveTasks();
        });
        
        // Add to list
        taskList.appendChild(li);
      });
    }
  }
});
```

---

## 📍 13. Debugging & Developer Tools  
Learning to debug is essential for becoming a good JavaScript developer.

### Browser DevTools
- **Elements panel**: Inspect and modify HTML/CSS
- **Console panel**: Run JavaScript and see errors
- **Sources panel**: Debug JavaScript with breakpoints
- **Network panel**: Monitor network requests
- **Application panel**: Inspect storage, service workers, etc.

### Console Methods
```javascript
// Basic logging
console.log("Basic information");
console.info("Similar to log, but for info");
console.warn("Warning message");
console.error("Error message");

// Grouping logs
console.group("User Details");
console.log("Name: Ram");
console.log("Age: 21");
console.groupEnd();

// Table format for arrays/objects
console.table(["apple", "banana", "orange"]);

// Timing operations
console.time("Loop time");
for(let i = 0; i < 1000000; i++) {
  // Some operation
}
console.timeEnd("Loop time");
```

### Debugging Techniques
1. **Using breakpoints**:
   - In browser: Open DevTools > Sources > Click line number
   - In code: Add `debugger;` statement

2. **Using watch expressions**:
   - Add variables to watch in the debugger to monitor their values

3. **Step through code**:
   - Step over: Execute current line and move to next
   - Step into: Enter function calls
   - Step out: Complete current function and return to caller

4. **Error handling**: Set DevTools to break on caught exceptions

---

## 📍 14. Frameworks & Libraries (Intro Only)  

### React.js
Most popular frontend library in 2025.
```javascript
// Simple React component
function Welcome() {
  return <h1>Hello, BCA Students!</h1>;
}
```

### Vue.js
Progressive framework, easy to integrate.
```javascript
// Simple Vue component
new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
});
```

### Angular
Full-featured framework for enterprise applications.

### Node.js
JavaScript runtime for backend development.
```javascript
// Simple Node.js server
const http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World!');
}).listen(8080);
```

---

## 📍 15. Practice Ideas  
Let's put our JavaScript skills to work!

### 1. To-do List Application
- Add, complete, and delete tasks
- Save tasks to localStorage
- Filter tasks by completed/active

### 2. Calculator
- Build a functional calculator
- Implement basic and advanced operations
- Add keyboard support

### 3. Form Validation
- Create a registration form
- Validate inputs in real-time
- Show appropriate error messages

### 4. Weather App
- Fetch data from a weather API
- Display current weather and forecast
- Allow users to search for different locations

### 5. Quiz Application
- Create a multi-question quiz
- Track and display scores
- Show correct answers

---

## 📦 Bonus: Hosting Your JS Projects  
Don't let your projects sit on your computer. Share them with the world!

### GitHub Pages (Free)
1. Push your project to a GitHub repository
2. Navigate to Settings > Pages
3. Select branch to deploy
4. Your site will be live at username.github.io/repository

### Netlify (Free tier)
1. Create an account on Netlify
2. Drag and drop your project folder
3. Or connect to your GitHub repository for continuous deployment
4. Custom domains available

### Vercel (Free tier)
1. Create an account on Vercel
2. Connect to your GitHub repository
3. Automatic deployments when you push changes
4. Great for React, Next.js applications

---

## 💡 Learning Tips  
- **Practice daily**: Even 30 minutes a day is better than 8 hours once a week
- **Build real projects**: Don't just follow tutorials, create your own projects
- **Read documentation**: MDN Web Docs is your best friend
- **Join communities**: Stack Overflow, Reddit r/javascript, Dev.to
- **Use browser DevTools**: Learning to debug will save you hours
- **Contribute to open source**: Great way to improve your skills
- **Teach others**: The best way to learn is to explain to someone else

### Learning Path Timeline
- **Week 1-2**: JavaScript basics, variables, control structures
- **Week 3-4**: Functions, arrays, objects
- **Week 5-6**: DOM manipulation, events
- **Week 7-8**: BOM, error handling, JSON
- **Week 9-10**: Modern JS, Fetch API
- **Week 11-12**: Final projects, deployment

---

## 📢 Share Your Progress  
Learning together is more fun and effective!

- Join our [Facebook Group](https://www.facebook.com/groups/nepalibcastudents)
- Connect on our [Telegram Channel](https://t.me/BCATU)
- Follow me for more tutorials:
  - [GitHub](https://github.com/mahendramahara)
  - [LinkedIn](https://www.linkedin.com/in/mahendramahara)

Share your projects, ask questions, and help fellow students. Remember, the community is here to support you!

---

## 🌟 Final Words of Motivation  
You're not just learning code — you're preparing for your future. JavaScript skills are in high demand, both in Nepal and globally. Every hour you spend practicing builds a foundation for your career success.

Don't worry about your pace. Focus on understanding and building. Break complex topics into manageable pieces. Celebrate your small wins along the way.

Remember, even experienced developers still Google basic syntax and face challenges daily. The difference is they've developed problem-solving skills through consistent practice.

I believe in you. Let's grow together on this exciting journey of JavaScript mastery! 💻🚀

---

### Resources to Continue Learning
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [FreeCodeCamp JavaScript Course](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/)
- [JavaScript.info](https://javascript.info/)
- [Eloquent JavaScript (free book)](https://eloquentjavascript.net/)