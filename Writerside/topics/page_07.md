# Functions

---

### 1. Functions: Let Us Reuse Code

Functions in JavaScript are blocks of reusable code designed to perform a specific task. They help in organizing code,
promoting reusability, and making programs more modular.

#### Declaration Syntax:

```javascript
function functionName(parameter1, parameter2, ...) {
  // Code to be executed
}
```

**Example:**

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

// Call the function
greet("John"); // Outputs: Hello, John!
```

Functions can take parameters (inputs) and can return values (outputs), making them versatile building blocks in
JavaScript programs.

### 2. Return: Get a Value Out of a Function

The `return` statement in a function allows you to send a value back to the code that called the function. This is
crucial for obtaining results or data from functions.

**Example:**

```javascript
function addNumbers(a, b) {
  return a + b;
}

let result = addNumbers(5, 3);
console.log(result); // Outputs: 8
```

The `return` statement not only provides a result but also exits the function, preventing further execution.

### 3. Parameters: Put Values into a Function

Parameters are placeholders for values that a function will receive when it is called. They allow functions to accept
input, making them more flexible and adaptable.

**Example:**

```javascript
function multiply(a, b) {
  return a * b;
}

let product = multiply(4, 7);
console.log(product); // Outputs: 28
```

Parameters act as variables within the function, taking on the values passed during the function call.

### 4. Improved Code for Rock, Paper, Scissors

Let's enhance the Rock, Paper, Scissors game by encapsulating the logic within a function.

#### Improved Rock, Paper, Scissors Function:

```javascript
<!DOCTYPE html>
<html>
  <head>
    <title>Rock Paper Scissors</title>
  </head>
  <body>
    <p>Rock Paper Scissors</p>
    <button onclick="
      playGame('rock');
    ">Rock</button>

    <button onclick="
      playGame('paper');
    ">Paper</button>

    <button onclick="
      playGame('scissors');
    ">Scissors</button>

    <script>
      function playGame(playerMove) {
        const computerMove = pickComputerMove();

        let result = '';

        if (playerMove === 'scissors') {
          if (computerMove === 'rock') {
            result = 'You lose.';
          } else if (computerMove === 'paper') {
            result = 'You win.';
          } else if (computerMove === 'scissors') {
            result = 'Tie.';
          }

        } else if (playerMove === 'paper') {
          if (computerMove === 'rock') {
            result = 'You win.';
          } else if (computerMove === 'paper') {
            result = 'Tie.';
          } else if (computerMove === 'scissors') {
            result = 'You lose.';
          }
          
        } else if (playerMove === 'rock') {
          if (computerMove === 'rock') {
            result = 'Tie.';
          } else if (computerMove === 'paper') {
            result = 'You lose.';
          } else if (computerMove === 'scissors') {
            result = 'You win.';
          }
        }

        alert(`You picked ${playerMove}. 
        Computer picked ${computerMove}. ${result}`);
      }

      function pickComputerMove() {
        const randomNumber = Math.random();

        let computerMove = '';

        if (randomNumber >= 0 && randomNumber < 1 / 3) {
          computerMove = 'rock';
        } else if (randomNumber >= 1 / 3 && randomNumber < 2 / 3) {
          computerMove = 'paper';
        } else if (randomNumber >= 2 / 3 && randomNumber < 1) {
          computerMove = 'scissors';
        }

        return computerMove;
      }
    </script>
  </body>
</html>
```

Encapsulating the game logic within a function makes the code more modular and reusable. You can easily call `playGame`
with different choices to play the game multiple times.

---

> This lesson covers the fundamental concepts of functions, the `return` statement, handling parameters, and applying
> these concepts to improve the code for the Rock, Paper, Scissors game. Understanding these topics enhances your
> ability
> to write structured, reusable, and efficient JavaScript code.

## 5. Exercises

**Exercise 7a:**
Create a function called 'greet' that displays the message 'Hello!' in the console. Call/run this function a few times
using: `greet();`

**Exercise 7b:**
Continuing from 7a, add a parameter called 'name' to the 'greet' function and display the message: 'Hello ${name}!' Call
the function a few times with different names: `greet('Simon');`

**Exercise 7c:**
Try calling `greet()` without a name (it will display 'Hello undefined!'). Modify the function so that if 'name' is
undefined, it will display 'Hi there!' instead. (Hint: use an if-statement. Since undefined is a falsy value, you can
use: `if (!name) { ... }` to check if 'name' is undefined).

**Exercise 7d:**
Create a function 'convertToFahrenheit(celsius)' that takes a number in degrees Celsius and returns a number in degrees
Fahrenheit.

* Formula: Fahrenheit = (Celsius * 9 / 5) + 32. `convertToFahrenheit(25) => 77`

**Exercise 7e:**
Create a function 'convertToCelsius(Fahrenheit)' that takes a number in degrees Fahrenheit and returns a number in
degrees Celsius.

* Formula: Celsius = (Fahrenheit - 32) * 5 / 9. `convertToCelsius(86) => 30`

**Exercise 7f:**
Create a function 'convertTemperature(degrees, unit)' that takes a number and a unit ('C' or 'F'), and converts it into
the other unit. `convertTemperature(25, 'C') => '77F'`, `convertTemperature(86, 'F') => '30C'. Note: return a string,
and try to reuse the functions from 7d and 7e.

**Exercise 7g:**
Create a copy of the Calculator project from exercise 5r (if you didn't do 5r, copy the code for 5r from the solutions).
Notice there's a lot of duplicated code in the buttons. Create a function 'updateCalculation' and reuse the code.

**Exercise 7h:**
Create a copy of the Cart Quantity project from exercise 6l. Create a function 'updateCartQuantity' and reuse the code.

**Exercise 7i:**
Modify 'updateCartQuantity' from 7h so that if the quantity is invalid, `alert();` and then `return;` (this is called an
early return). An early return makes our code cleaner because we can remove the 'else-if' / 'else'.