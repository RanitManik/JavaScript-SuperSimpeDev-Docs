# Booleans and if-statements

## 1. Boolean Values (true, false):

Boolean values (datatype) in JavaScript represent either `true` or `false`. They are fundamental for making decisions
and
controlling the flow of your program.

### Example:

```javascript
let isTrue = true;
let isFalse = false;

if (isTrue) {
  console.log("This statement is true!");
} else {
  console.log("This statement is false!");
}
```

## 2. If-Statements:

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

### Example:

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

## 3. Comparison Operators and Logical Operators:

### Comparison Operators (>, <, >=, <=, ===, !==):

Comparison operators are used to compare values. They return a boolean value based on whether the comparison is true or
false.

- **Greater Than (>):** Checks if the value on the left is greater than the value on the right.
- **Less Than (<):** Checks if the value on the left is less than the value on the right.
- **Greater Than or Equal To (>=):** Checks if the value on the left is greater than or equal to the value on the right.
- **Less Than or Equal To (<=):** Checks if the value on the left is less than or equal to the value on the right.
- **Equal To (===):** Checks if the values on both sides are equal in both value and type.
- **Not Equal To (!==):** Checks if the values on both sides are not equal in either value or type.

### Example:

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

### Logical Operators (&&, ||, !):

Logical operators are used to combine and manipulate boolean values.

- **Logical AND (&&):** Returns true if both operands are true.
- **Logical OR (||):** Returns true if at least one operand is true.
- **Logical NOT (!):** Returns the opposite boolean value.

### Example:

```javascript
let a = true;
let b = false;

console.log(a && b); // Outputs: false (true AND false)
console.log(a || b); // Outputs: true (true OR false)
console.log(!a); // Outputs: false (NOT true)
console.log(!b); // Outputs: true (NOT false)
```

#### Example:

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

## 4. Algorithms and Rock Paper Scissors:

Algorithms are step-by-step procedures or formulas for solving problems. In the context of programming, algorithms are
essential for designing logical and efficient solutions to various tasks. Let's explore the concept of algorithms by
creating a simple Rock Paper Scissors game.

### Rock Paper Scissors Algorithm:

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

### Rock Paper Scissors Example:

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

## 5. Truthy and Falsy Values:

In JavaScript, values are inherently truthy or falsy, which is important in conditions and evaluations.

### Example:

```javascript
let truthyValue = "Hello";
let falsyValue = 0;

if (truthyValue) {
  console.log("Truthy value is true");
} else {
  console.log("Truthy value is false");
}

if (falsyValue) {
  console.log("Falsy value is true");
} else {
  console.log("Falsy value is false");
}
```

## 6. Short-Circuit Evaluation in JavaScript

Short-circuit evaluation is a concept in programming languages, including JavaScript, where the evaluation of an
expression stops as soon as the result is determined. This can be particularly useful in logical expressions involving
the logical AND (`&&`) and logical OR (`||`) operators.

### Logical AND (`&&`) Short-Circuit

In a logical AND expression (`A && B`), if the first operand (`A`) evaluates to `false`, the entire expression is
already determined to be `false`, so the second operand (`B`) is not evaluated. This helps in optimizing code,
especially when the second operand involves expensive computations or function calls.

#### Example

```javascript
let isUserLoggedIn = false;
let userName = isUserLoggedIn && getUserInfo(); 
// getUserInfo() is not called if isUserLoggedIn is false
```

### Logical OR (`||`) Short-Circuit

In a logical OR expression (`A || B`), if the first operand (`A`) evaluates to `true`, the entire expression is already
determined to be `true`, and the second operand (`B`) is skipped. This is beneficial when the second operand might cause
side effects or unnecessary computations.

#### Example

```javascript
let defaultUserName = "Guest";
let inputUserName = ""; // Assume this is user input

let finalUserName = inputUserName || defaultUserName; 
// defaultUserName is used if inputUserName is falsy
```

### Using Short-Circuit Evaluation for Default Values

One common use of short-circuit evaluation is for setting default values. The logical OR operator is employed to provide
a default value when a variable is falsy.

#### Example

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

#### Example

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

#### Example

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

## 7. Exercises

**Exercise 6a:**

Create a variable called 'hour' and save the current hour of the day (use 24-hour format and save it as a number between
0 and 23).

* If the hour is between 6 and 12, display 'Good morning!' in the console.
* If the hour is between 13 and 17,
  display 'Good afternoon!' in the console.
* Otherwise, display 'Good night!' in the console.

**Exercise 6b:**

Continuing from 6a, try changing the value in the 'hour' variable to make it display different messages.

**Exercise 6c:**

Continuing from 6a, create a variable called 'name' and save your name inside (as a string). Update the if-statement to
display your name in each message.

* For example: `Good morning ${name}!`

**Exercise 6d:**

Imagine an amusement park that has a discount for children (6 years and younger) or seniors (65 years and older).

* Create a variable 'age' and save a person's age inside. Create an if-statement that checks if the person qualifies for
  a
  discount.
* If they do, display 'Discount' in the console.
* Otherwise, display 'No discount' in the console. Note: try to
  use the `||` operator in your solution.
* Try changing the 'age' variable to display different messages.

**Exercise 6e:**

Continuing from exercise 6d, let's say the discount is only available if it is not a holiday. Create a
variable: `const isHoliday = true;`. Update the code so that in order to get a discount, people must meet the age
requirement and it is also not a holiday. Note: && has a higher priority than || so you may need to use brackets () to
control which code gets done first. Try changing the value of isHoliday to display different messages.

**Exercise 6f:**

Generate a random number with `Math.random()`. Save it in a variable.

**Exercise 6g:**

Create an if-statement and check: If the number is less than 0.5, then display 'heads' in the console. Else display '
tails' in the console.

**Exercise 6h:**

Instead of displaying 'heads' or 'tails' in the console, save the result in a variable called 'result'.

**Exercise 6i:**

Let's say we're trying to guess the result. Create a variable called 'guess' and save your guess ('heads' or 'tails').
If your guess matches the result, display 'You win!' in the console. If your guess does not match the result, display '
You lose!'

**Exercise 6j:**

Instead of using if-statements in the previous exercises, try switching them into ternary operators (condition ? A : B).

**Exercise 6k:**

Let's say the cart has a maximum quantity of 10. Before updating the quantity, check if the quantity will be greater
than 10: If it will, display a popup saying 'The cart is full' and don't update the quantity. Otherwise, update the
quantity and console.log() it as usual.

**Exercise 6l:**

In exercises 5i - 5k, we created the 'Remove from cart', '-2', and '-3' buttons. Before updating the quantity, check if
it will go below 0: If it will, create a popup saying 'Not enough items in the cart' and don't update the quantity.
Otherwise, update the quantity and console.log() it as usual.