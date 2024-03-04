# Variables

## 1. Variables: A Way to Save Values

In JavaScript, variables serve as containers for storing data values. They provide a means to reference and manipulate
these values throughout your code. To declare a variable, you can use the `let`, `const`, or `var` keyword, followed by
the variable name.

```javascript
let x = 5; // Mutable variable
const PI = 3.14; // Immutable constant
var y = 10; // Old way, avoid using unless necessary

```

## 2. Re-assigning a Variable

Once a variable is declared, you can re-assign it to a new value using the assignment operator (`=`). This flexibility
allows you to update the content of a variable as your program runs.

```javascript
// Re-assigning a variable
let count = 10;
count = count + 1; // Incrementing the value
console.log(count); // Output: 11
```

## 3. Creating the Cart Quantity Feature

Variables are commonly used to implement features in applications. Let's create a simple example of a shopping cart
quantity feature using variables.

```html

<script>
    // Initialize totalQuantity variable
    let totalQuantity = 0;
</script>

<button onclick="
    console.log(`totalQuantity: ${totalQuantity++}`);">Add to Cart
</button>
<button onclick="
    console.log(`totalQuantity: ${totalQuantity += 2}`);">+2
</button>
<button onclick="
    console.log(`totalQuantity: ${totalQuantity += 3}`);">+3
</button>
<button onclick="
    totalQuantity = 0;
    console.log('totalQuantity: 0');">Reset
</button>

```

The provided code creates a simple interactive web page featuring a "Cart Quantity" functionality. The page includes
four buttons: "Add to Cart," "+2," "+3," and "Reset." Clicking these buttons triggers JavaScript actions that manipulate
and display the total quantity in the console.

Here's a brief summary of the functionality:

- **Add to Cart Button:** Increases the total quantity by 1 and logs the updated value to the console.

- **+2 Button:** Adds 2 to the total quantity and logs the updated value to the console.

- **+3 Button:** Increments the total quantity by 3 and logs the updated value to the console.

- **Reset Button:** Resets the total quantity to 0 and logs this reset value to the console.

The quantity updates are displayed in the console log, providing a simple demonstration of how JavaScript can
dynamically modify and track values on a webpage.

## 4. Shortcuts for Re-assigning a Variable

JavaScript provides shortcuts for common operations when re-assigning variables. These include `+=`, `-=`, `*=`,
and `/=`. They offer a concise way to update variable values.

```javascript
let total = 100;

// Shortcuts for re-assigning a variable
total += 20; // Equivalent to total = total + 20;
console.log("Total:", total); // Output: Total: 120
```

## 5. Naming Conventions and Best Practices

Follow meaningful naming conventions to enhance code readability. Use **camelCase** for variable names, and choose
descriptive names that convey the purpose of the variable.

```javascript
let userAge = 25;
let userName = "John Doe";
```

## 6. eval() Function

Certainly! In JavaScript, the `eval()` function is used to evaluate or execute a string of JavaScript code. It takes a
string as an argument and interprets it as JavaScript code. Here's a simple example:

```javascript
let x = 10;
let y = 20;
let result = eval('x + y');

console.log(result); // Outputs 30
```

In this example, the `eval()` function is used to dynamically execute the string `'x + y'`, which represents a
JavaScript expression. The result is then stored in the `result` variable and printed to the console.

It's important to note that the use of `eval()` should be approached with caution, as it can introduce security risks
and is generally considered a bad practice. It can execute arbitrary code and may lead to vulnerabilities such as code
injection. In most cases, it's better to find alternative, safer ways to achieve the desired functionality without
using `eval()`.

Understanding these fundamental concepts and best practices will lay a solid foundation for your journey into JavaScript
development. Experiment with these examples to reinforce your understanding and build your coding skills. Happy coding!
