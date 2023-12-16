# Numbers and Math Operations

## 1. Numbers and Math

JavaScript provides robust support for numerical operations, allowing you to perform various calculations within your
programs. Understanding the basics of numbers and math operations is crucial for any JavaScript developer.

### Numbers

In JavaScript, numbers can be integers or decimals (floats). For example:

```javascript
let integerNumber = 42;
let floatNumber = 3.14;
```

### Math Operations

JavaScript supports standard mathematical operations:

```javascript
let sum = 5 + 3;       // Addition
let difference = 10 - 4; // Subtraction
let product = 6 * 7;    // Multiplication
let quotient = 15 / 3;  // Division
```

## 2. Order of Operations and Brackets ( )

Understanding the order in which mathematical operations are performed is crucial. JavaScript follows the standard order
of operations (PEMDAS/BODMAS: Parentheses/Brackets, Exponents/Orders, Multiplication and Division, Addition and
Subtraction).

```javascript
let result = (2 + 3) * 4; // Parentheses take precedence
```

## 3. Handling Accuracy Issues in JavaScript Float Calculations

### Introduction

JavaScript, like many programming languages, uses floating-point numbers to represent decimal values. While this
facilitates a broad range of numerical operations, it also introduces the potential for inaccuracies in calculations
involving floating-point numbers. In this page, we'll explore why calculations using floats can be inaccurate in
JavaScript and discuss strategies to mitigate these issues.

### Understanding the Problem

The inaccuracy in floating-point calculations arises from the way computers represent real numbers in binary. Some
decimal numbers cannot be precisely represented in binary, leading to rounding errors. This can result in unexpected
behavior, especially in financial or scientific applications where precision is crucial.

#### Example:

```javascript
let result = 0.1 + 0.2;
console.log(result); // Output: 0.30000000000000004
```

### Strategies to Avoid Inaccuracy

#### 1. Use Integer Arithmetic

Performing calculations with integers can help avoid floating-point precision issues. If possible, work with integers
and only convert to floats when necessary.

```javascript
let totalCents = 10 + 20; // Perform calculations with integers
let resultInDollars = totalCents / 100; // Convert to float when necessary
console.log(resultInDollars); // Output: 0.3
```

#### 2. Use Decimal.js Library

The Decimal.js library provides a Decimal data type with arbitrary precision arithmetic. This can be especially useful
in scenarios where high precision is required.

```javascript
// Assuming Decimal.js library is imported
let a = new Decimal(0.1);
let b = new Decimal(0.2);
let result = a.plus(b);
console.log(result.toString()); // Output: 0.3
```

#### 3. Round Numbers Appropriately

Rounding numbers to a specific decimal place can help mitigate precision issues. However, be cautious with rounding, as
it may introduce its own set of problems.

```javascript
let result = 0.1 + 0.2;
result = Math.round(result * 100) / 100; // Round to two decimal places
console.log(result); // Output: 0.3
```

### Conclusion

Understanding the limitations of floating-point arithmetic in JavaScript is essential for writing robust and accurate
code. By adopting strategies like using integers, leveraging specialized libraries, and rounding numbers appropriately,
you can minimize the impact of precision issues in your calculations.

## 4. Math.round()

To mitigate floating-point inaccuracies, the `Math.round()` function can be used to round a number to the nearest
integer.

The `Math.round()` method rounds a number to the nearest integer.
2.49 will be rounded down (2), and 2.5 will be rounded up (3).

```javascript
let roundedNumber = Math.round(0.1 + 0.2); // Result: 0
let roundedNumber = Math.round(1 + 2.2); // Result: 3
let roundedNumber = Math.round(0.49); // Result: 0
let roundedNumber = Math.round(0.5); // Result: 1
```

In summary, mastering numbers and math operations in JavaScript is fundamental for writing effective and accurate code.
Understanding the order of operations and handling floating-point precision issues will enhance the reliability of your
programs.

## 5. Math.floor()

In JavaScript, the `Math.floor()` function is used to round down a decimal number to the nearest integer that is less
than or equal to the original argument. It
takes a single argument, which is the number you want to round down. Here's an example:

```javascript
let decimalNumber = 7.85;
let roundedDownNumber = Math.floor(decimalNumber);

console.log(roundedDownNumber); // Output: 7
```

In this example, `Math.floor()` is applied to `7.85`, and the result is `7` because it rounds down to the nearest
integer. It's important to note that `Math.floor()` always returns a whole number that is less than or equal to the
original decimal number.

If you have a negative decimal number, `Math.floor()` will round it to the smaller integer that is less than or equal to
the original number. For example:

```javascript
let negativeDecimalNumber = -4.25;
let roundedDownNegativeNumber = Math.floor(negativeDecimalNumber);

console.log(roundedDownNegativeNumber); // Output: -5
```

In this case, `Math.floor()` rounds down `-4.25` to `-5`.

## 6. Math.ceil()

In JavaScript, the `Math.ceil()` function is used to round a number up to the nearest integer that is greater than or
equal to the original argument. This function is part of
the `Math` object and takes a single argument, which is the number you want to round up. Here's a brief explanation and
example:

```javascript
let decimalNumber = 2.2;
let roundedUpNumber = Math.ceil(decimalNumber);

console.log(roundedUpNumber); // Output: 3
```

In this example, `Math.ceil()` is applied to the decimal number `2.2`, and the result is `3` because it rounds up to the
nearest integer that is greater than or equal to the argument.

If you have a negative decimal number, `Math.ceil()` will still round it up to the smallest integer that is greater than
or equal to the original number:

```javascript
let negativeDecimalNumber = -2.8;
let roundedUpNegativeNumber = Math.ceil(negativeDecimalNumber);

console.log(roundedUpNegativeNumber); // Output: -2
```

So, in both cases, whether the number is positive or negative, `Math.ceil()` rounds the number up to the next higher
integer.

## 7. Exercises

**Exercise 2a:**
At a restaurant, you order 1 soup for $10, 3 burgers for $8 each, and 1 ice cream for $5. Use JavaScript to calculate
the cost of the order.

**Exercise 2b:**
You're at a restaurant with 2 friends (3 people in total) and make the same order as 2a. Calculate how much each person
pays.

**Exercise 2c:**
Calculate the total cost of a toaster ($18.50) and 2 shirts ($7.50 each).

**Exercise 2d:**
Calculate a 10% tax for the total in exercise 2c.

**Exercise 2e:**
Calculate a 20% tax for the total in 2c (remember that 1% = 1/100, so 20% = 20 / 100 = 0.2).

**Order Summary:**

- a toaster ($18.99) | 1 t-shirt ($7.99 each) | 1 basketball ($20.95)

```
Items (3):              $47.93
Shipping & handling:    $4.99
Total before tax:       $52.92
Estimated tax (10%):    $5.29
Order total:            $58.21
```

**Exercise 2f:**
Calculate the cost of the products (before shipping and taxes). Hint: calculate in cents to avoid inaccuracies.

**Exercise 2g:**
Calculate the Total before tax.

**Exercise 2h:**
Calculate the 10% tax exactly. Hint: use `Math.round()`.

**Exercise 2i:**
Calculate Order total at the bottom. After finishing 2i, remove the toaster from your cart.

**Exercise 2j:**
Let's say we want to always round a number down (2.8 => 2). Using Google or an A.I. tool, search for the code to do
this.

**Exercise 2k:**
Let's always round a number up (2.2 => 3). Search how to do this.

**Exercise 2l:**
The temperature is 25°C. Calculate the temperature in Fahrenheit. (77)

**Exercise 2m:**
The temperature is 86°F. Calculate the temperature in Celsius. (30)

**Exercise 2n:**
The temperature is -5°C. Calculate the temperature in Fahrenheit. (23)
