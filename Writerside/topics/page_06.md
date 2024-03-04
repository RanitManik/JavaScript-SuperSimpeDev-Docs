# Booleans and if-statements

## 1. Boolean Values (true, false)

Boolean values (datatype) in JavaScript represent either `true` or `false`. They are fundamental for making decisions
and
controlling the flow of your program.

**Example:**

```javascript
let isTrue = true;
let isFalse = false;

if (isTrue) {
  console.log("This statement is true!");
} else {
  console.log("This statement is false!");
}
```

## 2. If-Statements

If-statements allow you to make decisions in your code based on certain conditions. They follow the syntax:

```javascript
if (condition) {
  // Code to be executed if the condition is true
} else if (anotherCondition) {
  // Code to be executed if the 'anotherCondition' is true
} else {
  // Code to be executed if none of the conditions are true
}
```

**Example:**

```javascript
let num = 10;

if (num > 10) {
  console.log("The number is greater than 10");
} else if (num < 10) {
  console.log("The number is less than 10");
} else {
  console.log("The number is equal to 10");
}
```

## 3. Comparison Operators and Logical Operators

### Comparison Operators (>, <, >=, <=, ===, !==)

Comparison operators are used to compare values. They return a boolean value based on whether the comparison is true or
false.

- **Greater Than (>):** Checks if the value on the left is greater than the value on the right.
- **Less Than (<):** Checks if the value on the left is less than the value on the right.
- **Greater Than or Equal To (>=):** Checks if the value on the left is greater than or equal to the value on the right.
- **Less Than or Equal To (<=):** Checks if the value on the left is less than or equal to the value on the right.
- **Equal To (===):** Checks if the values on both sides are equal in both value and type.
- **Not Equal To (!==):** Checks if the values on both sides are not equal in either value or type.

**Example:**

```javascript
let x = 5;
let y = 10;

console.log(x > y); // Outputs: false
console.log(x < y); // Outputs: true
console.log(x >= y); // Outputs: false
console.log(x <= y); // Outputs: true
console.log(x === y); // Outputs: false
console.log(x !== y); // Outputs: true
```

### Logical Operators (&&, ||, !)

Logical operators are used to combine and manipulate boolean values.

- **Logical AND (&&):** Returns true if both operands are true.
- **Logical OR (||):** Returns true if at least one operand is true.
- **Logical NOT (!):** Returns the opposite boolean value.

**Example:**

```javascript
let a = true;
let b = false;

console.log(a && b); // Outputs: false (true AND false)
console.log(a || b); // Outputs: true (true OR false)
console.log(!a); // Outputs: false (NOT true)
console.log(!b); // Outputs: true (NOT false)
```

**Example:**

```javascript
let age = 15;
let hasLicense = true;

if (age >= 18 || hasLicense) {
  console.log("You are eligible to drive.");
} else {
  console.log("You are not eligible to drive.");
}
```

In the above example, the person is eligible to drive if they are 18 years or older or if they already have a driver's
license. The `||` (OR) operator allows either condition to be true for the overall expression to be true.

## 4. Algorithms and Rock Paper Scissors

Algorithms are step-by-step procedures or formulas for solving problems. In the context of programming, algorithms are
essential for designing logical and efficient solutions to various tasks. Let's explore the concept of algorithms by
creating a simple Rock Paper Scissors game.

### Rock Paper Scissors Algorithm

The Rock Paper Scissors game involves two players making simultaneous choices among three possible options: rock, paper,
or scissors. The winner is determined by a set of rules: rock beats scissors, scissors beats paper, and paper beats
rock. The game can be implemented through a series of logical steps:

1. **Player Input:**
    - Obtain the user's choice (rock, paper, or scissors).
    - This can be achieved through user input or any other means of capturing the player's decision.

2. **Computer Input:**
    - Generate a random choice for the computer (rock, paper, or scissors).
    - This simulates the computer's decision-making process.

3. **Comparison:**
    - Compare the user's choice with the computer's choice based on the game rules.
    - Determine the winner or declare a tie.

4. **Display Result:**
    - Output the result of the game to the user.

### Rock Paper Scissors Example

```javascript
<!DOCTYPE html>
<html>
  <head>
    <title>Rock Paper Scissors</title>
  </head>
  <body>
    <p>Rock Paper Scissors</p>
    <button onclick="
      const randomNumber = Math.random();

      let computerMove = '';

      if (randomNumber >= 0 && randomNumber < 1 / 3) {
        computerMove = 'rock';
      } else if (randomNumber >= 1 / 3 && randomNumber < 2 / 3) {
        computerMove = 'paper';
      } else if (randomNumber >= 2 / 3 && randomNumber < 1) {
        computerMove = 'scissors';
      }

      let result = '';

      if (computerMove === 'rock') {
        result = 'Tie.';
      } else if (computerMove === 'paper') {
        result = 'You lose.';
      } else if (computerMove === 'scissors') {
        result = 'You win.';
      }

      alert(`You picked rock. Computer picked ${computerMove}. ${result}`);
    ">Rock</button>

    <button onclick="
      const randomNumber = Math.random();

      let computerMove = '';

      if (randomNumber >= 0 && randomNumber < 1 / 3) {
        computerMove = 'rock';
      } else if (randomNumber >= 1 / 3 && randomNumber < 2 / 3) {
        computerMove = 'paper';
      } else if (randomNumber >= 2 / 3 && randomNumber < 1) {
        computerMove = 'scissors';
      }

      let result = '';

      if (computerMove === 'rock') {
        result = 'You win.';
      } else if (computerMove === 'paper') {
        result = 'Tie.';
      } else if (computerMove === 'scissors') {
        result = 'You lose.';
      }

      alert(`You picked paper. Computer picked ${computerMove}. ${result}`);
    ">Paper</button>

    <button onclick="
      const randomNumber = Math.random();

      let computerMove = '';

      if (randomNumber >= 0 && randomNumber < 1 / 3) {
        computerMove = 'rock';
      } else if (randomNumber >= 1 / 3 && randomNumber < 2 / 3) {
        computerMove = 'paper';
      } else if (randomNumber >= 2 / 3 && randomNumber < 1) {
        computerMove = 'scissors';
      }

      let result = '';

      if (computerMove === 'rock') {
        result = 'You lose.';
      } else if (computerMove === 'paper') {
        result = 'You win.';
      } else if (computerMove === 'scissors') {
        result = 'Tie.';
      }

      alert(`You picked scissors. 
      Computer picked ${computerMove}. ${result}`);
    ">Scissors</button>
  </body>
</html>
```

In this example, the algorithm encompasses the entire process of the Rock Paper Scissors game, from obtaining user input
and generating computer input to determining the winner and displaying the result. Algorithms are fundamental to
problem-solving in programming, providing a structured approach to solving specific tasks efficiently.

## 5. Truthy and Falsy Values

In JavaScript, truthy and falsy values are related to the concept of boolean evaluation. Every value in JavaScript has
an inherent boolean value, either true or false, when used in a boolean context (like in an `if` statement or as a
condition in a loop).

**Truthy Values:**
Values that are considered truthy evaluate to `true` in a boolean context. Examples of truthy values include:

1. All non-empty strings
2. All numbers except 0
3. Arrays (even if they are empty)
4. Objects
5. Functions

**Falsy Values:**
Conversely, falsy values are those that evaluate to `false` in a boolean context. Examples of falsy values include:

1. The empty string (`''`)
2. The number `0`
3. `NaN` (Not a Number)
4. `null`
5. `undefined`
6. `false`

Understanding truthy and falsy values is crucial in JavaScript programming, especially when dealing with conditional
statements, as it allows you to write more concise and expressive code. For example:

```javascript
let myVar = "Hello, World!";

if (myVar) {
    console.log("This will be executed because myVar is truthy.");
} else {
    console.log("This won't be executed.");
}
```

In this example, the code inside the `if` block will be executed because the string `"Hello, World!"` is a truthy value.

## 6. Short-Circuit Evaluation in JavaScript

Short-circuit evaluation is a concept in programming languages, including JavaScript, where the evaluation of an
expression stops as soon as the result is determined. This can be particularly useful in logical expressions involving
the logical AND (`&&`) and logical OR (`||`) operators.

### Logical AND (`&&`) Short-Circuit

In a logical AND expression (`A && B`), if the first operand (`A`) evaluates to `false`, the entire expression is
already determined to be `false`, so the second operand (`B`) is not evaluated. This helps in optimizing code,
especially when the second operand involves expensive computations or function calls.

**Example:**

```javascript
let isUserLoggedIn = false;
let userName = isUserLoggedIn && getUserInfo(); 
// getUserInfo() is not called if isUserLoggedIn is false
```

### Logical OR (`||`) Short-Circuit

In a logical OR expression (`A || B`), if the first operand (`A`) evaluates to `true`, the entire expression is already
determined to be `true`, and the second operand (`B`) is skipped. This is beneficial when the second operand might cause
side effects or unnecessary computations.

**Example:**

```javascript
let defaultUserName = "Guest";
let inputUserName = ""; // Assume this is user input

let finalUserName = inputUserName || defaultUserName; 
// defaultUserName is used if inputUserName is falsy
```

### Using Short-Circuit Evaluation for Default Values

One common use of short-circuit evaluation is for setting default values. The logical OR operator is employed to provide
a default value when a variable is falsy.

**Example:**

```javascript
function greetUser(name) {
  name = name || "Guest"; // If name is falsy, use "Guest" as the default
  console.log(`Hello, ${name}!`);
}

greetUser("John"); // Outputs: Hello, John!
greetUser(); // Outputs: Hello, Guest! (uses the default value)
```

### Using the Guard Operator

The guard operator is particularly useful when you want to perform an action or set a value only if a certain condition
is truthy. It prevents the execution of subsequent code if the condition is falsy, acting as a guard against unnecessary
operations.

**Example:**

```javascript
let isLoggedIn = true;
let userInfo = isLoggedIn && getUserInfo();

// getUserInfo() is only called if isLoggedIn is true
// If isLoggedIn is false, userInfo remains undefined
```

In this example, `getUserInfo()` is executed only if `isLoggedIn` is `true`. This prevents unnecessary function calls or
operations when the condition is not met.

### Guard Operator for Default Values

The guard operator is often used for providing default values, similar to the logical OR (`||`) short-circuit approach.

**Example:**

```javascript
function greetUser(name) {
  name = name && name.trim(); // Trim whitespace only if name is truthy
  console.log(`Hello, ${name || "Guest"}!`);
}

greetUser("   John   "); // Outputs: Hello, John!
greetUser(); // Outputs: Hello, Guest! (uses the default value)
```

In this case, the `name.trim()` is only executed if `name` is truthy. If `name` is falsy, the guard operator prevents
the call to `trim()`, avoiding potential errors.

While short-circuit evaluation can lead to more concise and efficient code, it's essential to be cautious. In some
cases, you might want to ensure that both operands are evaluated, especially if there are side effects in the
expressions.

> This comprehensive section covers fundamental concepts in JavaScript, from boolean values and if-statements to
> operators, algorithms, and practical examples like Rock Paper Scissors. Understanding these topics is essential for
> mastering JavaScript development.