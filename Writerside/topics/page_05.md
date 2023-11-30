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

Understanding these fundamental concepts and best practices will lay a solid foundation for your journey into JavaScript
development. Experiment with these examples to reinforce your understanding and build your coding skills. Happy coding!

## 6. Exercises

**Exercise 5a:**
Create a `<script>` element. Inside the `<script>`, create a variable called 'name', and save your name in this
variable (as a string).

**Exercise 5b:**
Continuing from 5a, display the message 'My name is: ${name}' in the console (insert the 'name' variable created in 5a
into this message).

**Exercise 5c:**
At a restaurant, you order 1 coffee ($5), 2 bagels ($3 each), and 1 soup ($9). Calculate the cost and save it in a
variable called 'cost'.

**Exercise 5d:**
Continuing from 5c, display 'Cost of food: $${cost}' in the console.

**Exercise 5e:**
Let's say the restaurant charges a 10% tax. Using the 'cost' variable from 5c, calculate the tax (hint: multiply by
0.1), and save the result in a variable.

**Exercise 5f:**
Continuing from 5e, display 'Tax (10%): $${tax}' in the console.

**Exercise 5g:**
Continuing from 5f, calculate the total (cost + tax), save it in a variable called 'totalCost', and display the
message 'Total cost: $${totalCost}' in the console.

**Exercise 5h:**
In the Cart Quantity project, add 2 more buttons '+4' and '+5', which increase the quantity by 4 and 5 when you click
them. Try using `+=`.

**Exercise 5i:**
In the Cart Quantity project, add a button 'Remove from cart', which decreases the cart quantity by 1.

**Exercise 5j:**
Add 2 buttons '-2' and '-3', which decrease the quantity by 2 and 3.

**Exercise 5k:**
Use the shortcuts `--` and `-=` in 5i and 5j.

**Exercise 5l:**
Add the HTML structure ( `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`). Add a `<title>` with the text 'Calculator'.

**Exercise 5m:**
Create these 5 buttons: `1` `2` `3` `+` `=`

**Exercise 5n:**
Create a `<script>`, create a variable called 'calculation', and save an empty string inside: `let calculation = "";` (
This variable will store the calculation like '1 + 2' or '11 + 2 + 2')

**Exercise 5o:**
When we click the '1' button:

- Add the string '1' to the calculation variable: `calculation += '1';
- Display the calculation in the console: `console.log(calculation);`

**Exercise 5p:**
Do the same for the '2', '3', and '+' buttons (add ' +' instead of '+').

**Exercise 5q:**
When we click the '=' button, use the code:

- `eval(calculation);`
- Save the result back in 'calculation': `calculation = eval(calculation);`
- Display the result in the console: `console.log(calculation);`

**Exercise 5r:**
Create the rest of the buttons in the calculator. To create multiple rows of buttons, put the buttons inside elements
like this:

```html

<p>
    <button>1</button>
    <button>2</button>
</p>
<p>
    <button>4</button>
    <button>5</button>
</p>
```