# HTML, CSS, and console.log

## 1. Reviewed basics of HTML and CSS

Before diving into JavaScript, it's crucial to have a solid grasp of HTML and CSS, the foundational elements of web
development.

### HTML Basics:

- HTML (Hypertext Markup Language) structures web content.
- Understand HTML tags, elements, attributes, and document structure.
- Learn to create headings, paragraphs, lists, links, and other essential HTML elements.

### CSS Basics:

- CSS (Cascading Style Sheets) styles and layouts.
- Apply styles to HTML elements, control layout, and manage responsiveness.
- Comprehend selectors, properties, values, and the box model.

## 2. Set up Visual Studio Code (VSCode)

Visual Studio Code is a popular, lightweight code editor. Configuring it for JavaScript development involves:

- **Installation:**
    - Download and install [VSCode](https://code.visualstudio.com/download) from the official website.
    - Open VSCode and explore its user-friendly interface.

- **Extensions:**
    - Install extensions for JavaScript development, such as ESLint for code linting and Prettier for code formatting.
    - Personalize settings for a tailored development environment.

- **Key Features:**
    - Familiarize yourself with key features like IntelliSense, integrated terminal, and version control.

## 3. Loading JavaScript within HTML

To integrate JavaScript into an HTML document:

- Use the `<script>` tag to include JavaScript code within the HTML document.
- Place the `<script>` tag in the `<head>` or `<body>` section.

Here's a simple and basic example of loading JavaScript within an HTML document using the `<script>` tag:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript in HTML Example</title>
</head>
<body>

<h1>Hello, HTML with JavaScript!</h1>

<!-- Using the <script> tag to load JavaScript -->
<script>
    // JavaScript code goes here
    var message = "Welcome to JavaScript!";
    console.log(message);
    alert(message);
</script>

</body>
</html>
```

In this example:

- The `<script>` tag is used to include JavaScript code directly within the HTML document.
- Inside the `<script>` tag, a simple JavaScript code block is provided.
- The JavaScript code creates a variable `message` with the value "Welcome to JavaScript!".
- It then logs the message to the browser's console using `console.log`.
- Finally, an `alert` is triggered, displaying a pop-up with the message.

This is a basic example of how you can embed JavaScript directly into an HTML document using the `<script>` tag.
Typically, you can also link to external JavaScript files for more organized code structure. We will learn to do that in
our next sections.

## 4. Handling Click Events with `onclick` and `alert`

The `onclick` event in JavaScript triggers a function when an HTML element is clicked, adding interactivity to your
webpage.

### Using `onclick` Attribute:

You can use the `onclick` attribute directly in HTML to associate a function with a click event, means you can write
javascript code between the double quotes which will trigger when the `onclick` event take place Here's an example:

```html

<button onclick="console.log('Hello, world!')">Click me</button>
```

In this example, `console.log('Hello, world!')` will print 'Hello, world!' in the browser's console when the button is
clicked.

```html

<button onclick="alert('Hello, world!')">Click me</button>
```

This example will display an alert with the message 'Hello, world!' when the button is clicked.

#### Summary:

- The `onclick` event handles click events on HTML elements.
- It can be applied directly in HTML using the `onclick` attribute or through JavaScript with `addEventListener`.
- Dynamic event handling is achieved by passing parameters to functions.

Understanding how to use the `onclick` event is fundamental for creating interactive web pages, allowing you to respond
to user actions effectively.

## 5. Comments

Comments in JavaScript serve as explanatory notes:

- **Single-line Comment:**
  ```javascript
  // This is a single-line comment
  ```

- **Multi-line Comment:**
  ```javascript
  /*
   This is a multi-line
   comment
  */
  ```

- Use comments to explain code logic, provide context, or temporarily disable code.

## 6. `console.log`

`console.log` is a vital tool for debugging and logging messages to the browser's console:

- **Debugging:**
    - Place `console.log` statements strategically to output variable values or messages.
  ```javascript
  var message = 'Hello, console!';
  console.log(message); // Hello, console!
  ```

- **Viewing Output:**
    - Open the browser's developer tools to view the console output.
    - Helpful for identifying errors and understanding program flow.

These detailed explanations aim to provide a comprehensive understanding of each topic. Feel free to incorporate these
details into your documentation, and let me know if there's anything else you need!

## 7. Exercises

**Exercise 4a:**
Create a button with the text 'Click' inside.

**Exercise 4b:**
Create 2 buttons. 1 with your name and 1 with your favorite food.

**Exercise 4c:**
Create a paragraph with the text 'Hello, world!' inside.

```
Hello, world!
```

**Exercise 4d:**
Continuing from exercise 4c, create a paragraph below the previous paragraph and write something you did today.

```
Hello, world!
Today I went to the grocery store to buy some eggs and vegetables.
```

**Exercise 4a:**
Create a paragraph with the text "Hello, world!" and use CSS to set the text color to blue.

**Exercise 4b:**
Create an unordered list with three list items: "Apple," "Banana," and "Orange." Apply CSS to give the list items a
green color.

**Exercise 4c:**
Create a div with the id "box" and apply CSS to give it a red border with a thickness of 2px and a solid style.

**Exercise 4d:**
Create a heading with the text "My Web Page" and apply CSS to center the text and give it a font size of 24px.

**Exercise 4e:**
Create 2 buttons "Add to cart" and "Buy now." Use CSS to give them yellow and orange background colors.

**Exercise 4f:**
Add the HTML structure to exercise 4e and change the title at the top of the tab to 'Buttons'.

**Exercise 4g:**
Continuing from 4f, change the title at the top of the tab to 'Buttons'.

**Exercise 4h:**
Continuing from 4g, add a `<script>` element so that when the page loads, it displays the message 'Welcome!' in the
Console.

**Exercise 4i:**
Using HTML and CSS, attempt to copy the design.

```text
Adults Plain Cotton T-shirt
Price: $7.99
Add to cart     Buy now
```

**Exercise 4j:**
Continuing from 4i, add `onclick` attributes to the two buttons:

- When clicking 'Add to cart', create a popup with the text 'Added'.
- When clicking 'Buy now', display the message 'Loading...' in the Console, and then create a popup with the text '
  Purchased'.
