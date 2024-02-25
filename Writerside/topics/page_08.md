# JavaScript Objects

## 1. Creating Objects

JavaScript objects are a fundamental data structure that allows developers to store and organize data efficiently using
key-value pairs. Objects in JavaScript provide a flexible and powerful way to represent and manipulate complex data.

**Basic Structure**

In JavaScript, objects are created using curly braces `{}`. Key-value pairs are defined within the braces, and
individual pairs are separated by commas. Here's an example:

```javascript
// Creating an object
let person = {
  name: "Ranit",
  age: 20,
  profession: "Developer",
  location: "Mecheda, West Bengal"
};
```

## 2. Accessing Object Properties

Once an object is created, you can access its properties using dot notation or square brackets. Here's how you can
access properties:

```javascript
// Accessing object properties
console.log(person.name); // Output: Ranit
console.log(person["age"]);  // Output: 20
```

## 3. Modifying and Adding Properties

Object properties can be modified and new properties can be added dynamically. Here's an example:

```javascript
// Modifying object properties
person.age = 21;

// Adding a new property
person.language = "Bengali";
```

## 4. Deleting Properties

If you need to remove a property from an object, you can use the `delete` keyword. Here's how it's done:

```javascript
// Deleting a property
delete person.location;
```

## 5. Checking Property Existence

To check if a property exists in an object, you can use the `in` operator. Here's an example:

```javascript
// Checking if a property exists
if ("profession" in person) {
  console.log("Profession:", person.profession);
} else {
  console.log("Profession not found.");
}
```

## 6. JSON (JavaScript Object Notation)

JSON, standing for JavaScript Object Notation, is a lightweight data interchange format. It is easy for humans to read
and write and easy for machines to parse and generate. JSON is a common data format with diverse uses in electronic data
interchange, including web applications and web services.

**Basic Structure**

JSON data is represented as key-value pairs, similar to JavaScript object literals.

```json
{
  "name": "John Doe",
  "age": 30,
  "city": "New York"
}
```

- **Object**: Enclosed in curly braces `{}`, representing an unordered set of key-value pairs.
- **Key**: A string representing the name of the property.
- **Value**: Can be a string, number, object, array, boolean, or `null`.

### 7. Usage in JavaScript

JavaScript provides methods to parse JSON strings into JavaScript objects and stringify JavaScript objects into JSON
strings.

#### 8. Parsing JSON

```javascript
const jsonString = '{"name": "John Doe", "age": 30, "city": "New York"}';

// Parse JSON string into JavaScript object
const parsedObject = JSON.parse(jsonString);

console.log(parsedObject.name); // Output: John Doe
```

#### 9. Stringifying JavaScript Objects

```javascript
const myObject = {
  name: "Jane Doe",
  age: 25,
  city: "San Francisco"
};

// Convert JavaScript object to JSON string
const jsonStringified = JSON.stringify(myObject);

console.log(jsonStringified);
// Output: {"name":"Jane Doe","age":25,"city":"San Francisco"}
```

## 10. localStorage

localStorage is a type of web storage that allows you to store key-value pairs in a web browser with no expiration time.
The data stored in localStorage persists even after the browser is closed and reopened.

### 11. Basic Usage

```javascript
// Storing data in localStorage
localStorage.setItem("username", "john_doe");

// Retrieving data from localStorage
const storedUsername = localStorage.getItem("username");

console.log(storedUsername); // Output: john_doe
```

### 12. Limitations

- **Storage Size**: localStorage has a size limit (usually 5 MB per domain).
- **Data Type**: Values stored in localStorage are always strings. If you need to store other data types, you should
  convert them to strings before storing and parse them when retrieving.

### 13. Example: Storing and Retrieving an Object

```javascript
const userObject = {
  username: "jane_doe",
  age: 28,
  isAdmin: true
};

// Convert the object to a JSON string before storing
localStorage.setItem("user", JSON.stringify(userObject));

// Retrieve and parse the JSON string when needed
const storedUser = JSON.parse(localStorage.getItem("user"));

console.log(storedUser.username); // Output: jane_doe
```

In this example, we use JSON.stringify to convert the object to a JSON string before storing it in localStorage. Later,
we use JSON.parse to convert the JSON string back to a JavaScript object when retrieving it. This allows us to store and
retrieve more complex data structures in localStorage.

## 14. More Details

### Null:

In JavaScript, `null` is a primitive data type that represents the intentional absence of any object value. It is often
used to indicate that a variable or object property does not currently have a meaningful value. For example:

```javascript
let myVariable = null;
```

Here, `myVariable` is explicitly set to `null`, indicating that it doesn't point to any valid object.

### Auto-boxing:

Auto-boxing in JavaScript refers to the automatic conversion of primitive data types to their corresponding object
wrapper types. This happens when a primitive value is used in a context where an object is expected. For instance:

```javascript
// Auto-boxing with numbers
let numPrimitive = 42; // primitive number
let numObject = new Number(numPrimitive); 
// automatically converted to Number object

// Auto-boxing with strings
let strPrimitive = "Hello, World!"; // primitive string
let strObject = new String(strPrimitive); 
// automatically converted to String object
```

In most cases, JavaScript handles this conversion implicitly, making it seamless for developers.

### References:

In JavaScript, objects are reference types. When you assign an object to a variable or pass it as a parameter to a
function, you are dealing with a reference to the object, not a copy of the object itself. Consider the following
example:

```javascript
// Creating an object
let originalObject = { key: "value" };

// Assigning the object to another variable
let referenceObject = originalObject;

// Modifying the referenceObject also modifies originalObject
referenceObject.key = "updated value";

console.log(originalObject.key); // Outputs: "updated value"
```

Here, both `originalObject` and `referenceObject` point to the same underlying object. Modifying one affects the other
because they share the same reference.

Understanding these concepts is crucial for effective JavaScript programming, especially when dealing with variables,
data types, and object manipulation.

## 15. Shortcuts

### Destructuring

Destructuring assignment allows you to extract values from objects and arrays and assign them to variables in a concise
way. Here's an example:

```javascript
// Destructuring assignment with objects
const { name, age } = person;
console.log(name, age); // Output: Ranit 21

// Destructuring assignment with arrays
const numbers = [1, 2, 3];
const [first, second] = numbers;
console.log(first, second); // Output: 1 2
```

### Shorthand Property and Method

JavaScript provides shorthand syntax for defining properties and methods in objects.

#### Shorthand Property

```javascript
const profession = "Developer";

// Shorthand property
const person = {
  name,
  age: 21,
  profession
};
```

#### Shorthand Method

```javascript
// Shorthand method
const calculator = {
  add(a, b) {
    return a + b;
  },
  subtract(a, b) {
    return a - b;
  }
};

console.log(calculator.add(5, 3)); // Output: 8
console.log(calculator.subtract(8, 3)); // Output: 5
```

These shortcuts make the code more concise and readable. Destructuring simplifies the extraction of values, while
shorthand syntax enhances the definition of object properties and methods.

## 16. Exercises

**Exercise 8a:**
Let's say in the Amazon project, we have a basketball product. This
product has a name of 'basketball', a price of 2095 cents. Create an
object to represent this product and display it in the console.

**Exercise 8b:**
Continuing from 8a, let's say we want to increase the price by 500
cents. Use dot notation to increase the price, and display the
updated object in the console.

**Exercise 8c:**
Using bracket notation, add a property 'delivery-time' to the object
with the value '3 days'. Display the updated object in the console.

**Exercise 8d:**
Create a function `comparePrice(product1, product2)`, which takes 2
products (with 'name' and 'price' properties) and returns the product
that is less expensive. Create 2 products and try out the function.

**Exercise 8e:**
Create a function `isSameProduct(productl, product2)`, which returns
true if 2 products have the same values inside ('name' and 'price').
If not, return false. Create 2 products and try out the function.
(Hint: objects are references so you can't compare them directly).

**Exercise 8f:**
Using Google or an A.I. tool, search how to convert a string to all
lowercase with JavaScript ('Good Morning' => 'good morning')

**Exercise 8g:**
Search how to repeat a string many times ('test' 2 times => 'testtest')

**Exercise 8h:**
We'll add localStorage to the calculator project. First, make a copy of
the project from exercise 7g (see the solution for 7g if needed).

- Whenever we update the calculation, save it using `.setltem()`
- When the page is loaded, get the calculation using `.getltem()`
- Use a default value of `''` if a calculation doesn't exist in local storage

**Exercise 8i:**
We'll improve the coin flip game from exercise 6j to be like the rock
paper scissors game.

- Copy the code from exercise 6j (see the solution for 6j if needed).

- Create 2 buttons to play the game - `heads` and `tails`
- When clicking 'heads' play the game with guess = 'heads'
- When clicking 'tails' play the game with guess = 'tails'
- Create a function 'playGame(guess)' to reuse the code

**Exercise 8j:**
Create a score object { wins: 0, losses: 0 }, update the score each time
after playing, and display the score in the console.

**Exercise 8k:**
Use localStorage to save and load the score (hint: you'll need to use
`JSON.stringify()` to convert the score object to a string).