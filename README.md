# 🚀 Assignment: Mastering JavaScript Fundamentals

Welcome to your next step toward JavaScript mastery! In this assignment, you'll explore essential concepts that form the backbone of interactive, dynamic web pages—functions, loops, and the Document Object Model (DOM). Ready to code like a pro? Let’s dive in.

---

## 🎯 Part 1: Mastering JavaScript Basics

Start with the building blocks of JavaScript—variables, data types, operators, and conditionals. You’ll write a few simple programs that capture user input, make decisions using `if/else`, and output results using `console.log()` or by modifying the webpage content.

**Goal:** Demonstrate your understanding of how JavaScript flows, processes logic, and interacts with data.

---

## ❤️ Part 2: JavaScript Functions — The Heart of Reusability

Functions are your best friends in programming. Write a few custom functions that take inputs, process them, and return or display results. You’ll also create functions for common tasks (like calculating totals, formatting strings, or toggling content).

**Goal:** Build reusable blocks of logic that make your code cleaner, smarter, and DRY (Don't Repeat Yourself).

---

## 🔁 Part 3: JavaScript Loops — Embrace the Power of Repetition!

Use `for`, `while`, or `forEach` loops to solve repetitive tasks like iterating through arrays, generating dynamic content, or simulating simple countdowns or animations.

**Goal:** Practice controlling flow with repetition and iteration—key to working with lists, animations, and form elements.

---

## 🌐 Part 4: Mastering the DOM with JavaScript

It’s time to bring your page to life! Use JavaScript to select elements, respond to user actions, and dynamically update the content of your web page. Tasks may include changing text, toggling classes, listening to click events, or creating elements on the fly.

**Goal:** Show your skill in making a static HTML page interactive using pure JavaScript and DOM manipulation.

---

## Deliverables

* A single project folder containing:

  * `index.html` — your structured HTML content
  * `style.css` — (optional) if you'd like to style your content
  * `script.js` — your JavaScript file including:

    * Variable declarations and conditionals (Part 1)
    * At least 2 custom functions (Part 2)
    * At least 2 loop examples (Part 3)
    * At least 3 DOM interactions (Part 4)

Each part of the assignment should be clearly commented and organized.

---

project-folder/
  ├── index.html
  ├── style.css
  └── script.js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Beginner JavaScript Project</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1 id="main-title">Welcome to My Beginner Project</h1>

  <!-- Buttons to trigger JavaScript functions -->
  <button id="greet-btn">Click to Greet</button>
  <button id="loop-btn">Show Loop Output</button>
  <button id="color-btn">Change Title Color</button>

  <!-- Area to show outputs -->
  <div id="output"></div>

  <script src="script.js"></script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}

button {
  margin: 10px;
  padding: 10px 15px;
  font-size: 16px;
  cursor: pointer;
}

#output {
  margin-top: 20px;
  font-size: 18px;
  color: darkblue;
}

// ===============================
// Part 1: Variables & Conditionals
// ===============================
let userName = "Shina";
let isLoggedIn = true;

// Simple conditional
if (isLoggedIn) {
  console.log("Welcome, " + userName + "!");
} else {
  console.log("Please log in.");
}

// ===============================
// Part 2: Functions
// ===============================

// Function 1: Display a greeting
function greetUser(name) {
  return "Hello, " + name + "! Welcome to the project.";
}

// Function 2: Add two numbers
function addNumbers(a, b) {
  return a + b;
}

// ===============================
// Part 3: Loops
// ===============================

// Example 1: For loop
function showNumbers() {
  let output = "";
  for (let i = 1; i <= 5; i++) {
    output += "Number: " + i + "<br>";
  }
  return output;
}

// Example 2: While loop
function showEvenNumbers() {
  let output = "";
  let num = 2;
  while (num <= 10) {
    output += "Even Number: " + num + "<br>";
    num += 2;
  }
  return output;
}

// ===============================
// Part 4: DOM Interactions
// ===============================

// DOM 1: Greet button
document.getElementById("greet-btn").addEventListener("click", function() {
  document.getElementById("output").innerHTML = greetUser(userName);
});

// DOM 2: Loop button
document.getElementById("loop-btn").addEventListener("click", function() {
  document.getElementById("output").innerHTML = showNumbers() + showEvenNumbers();
});

// DOM 3: Change title color
document.getElementById("color-btn").addEventListener("click", function() {
  document.getElementById("main-title").style.color = "green";
});

