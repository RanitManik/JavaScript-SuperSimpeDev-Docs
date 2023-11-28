# Writing and Running Code

## 1. Giving Instructions to a Computer

JavaScript is a versatile programming language that allows you to give instructions to a computer, making web pages
interactive and dynamic. As a client-side scripting language, it is primarily used for enhancing the user experience
within web browsers. JavaScript enables developers to create responsive and engaging web applications by manipulating
the content and behavior of HTML and CSS.

## 2. Writing JavaScript Code

To write JavaScript code, you can embed it directly within your HTML document or include it in a separate JavaScript
file. The code consists of a series of instructions that the browser executes in a sequential order. JavaScript is known
for its flexibility, supporting both procedural and object-oriented programming paradigms. You can use it to perform
calculations, manipulate data, and respond to user interactions.

Here's a simple example of JavaScript code that displays a message in the browser:

```javascript
// JavaScript code to display a message
var greeting = "Hello, JavaScript!";
console.log(greeting);
```

In this example, a variable `greeting` is declared, assigned a string value, and then the message is logged to the
console using `console.log()`.

## 3. Running Our Code Using the Console

The browser console is a powerful tool for testing and debugging JavaScript code. To run your code, open the browser's
developer tools (usually by pressing `F12` or right-clicking on the page and selecting "Inspect"), navigate to the "
Console" tab, and enter your JavaScript code directly.

For example, you can copy and paste the previous code snippet into the console and press `Enter` to see the output. The
console is an invaluable resource for inspecting variables, identifying errors, and understanding how your code is
executed.

## 4. Syntax

JavaScript syntax refers to the set of rules that dictate how programs written in JavaScript should be structured.
Proper syntax is crucial for the code to be interpreted correctly by the browser. We will be learning about them in
details in our next sections. Here are some fundamental syntax
elements:

- **Variables:** Used to store and manipulate data.

  ```javascript
  var x = 10;
  ```

- **Functions:** Blocks of reusable code.

  ```javascript
  function addNumbers(a, b) {
      return a + b;
  }
  ```

- **Conditional Statements:** Control the flow of the program.

  ```javascript
  if (x > 5) {
      console.log("x is greater than 5");
  } else {
      console.log("x is not greater than 5");
  }
  ```

- **Loops:** Repeat code execution.

  ```javascript
  for (var i = 0; i < 5; i++) {
      console.log(i);
  }
  ```

Understanding and applying proper syntax is essential for writing effective and error-free JavaScript code. Regular
practice and exploration of JavaScript's features will help you become proficient in crafting dynamic and interactive
web applications.