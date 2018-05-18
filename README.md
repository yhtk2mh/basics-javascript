# JavaScript Programming Concepts For QA

For a Manual Tester or QA, programming can be a intimidating. But don't worry. When it comes to test automation, there is only a small subset of programming that we really need to know in order to get started.

In the ocean full of beautiful programming concepts out there, here are the ones we'll focus on to get started:

## Types of Objects

- Strings
- Integers
- Data Structures
- Booleans, etc.

## Object Structures

- **Variables**

  Variables are like containers which help us to store and retrive values.

  Rules to follow when creating variables.
  - Should be prepended with word `var` or `const` or `let`.
  - Should start with letter.
  - Is not case sensitive.
  - Should not be a keyword or reserved word in Javascript.
  - Can be of one or more words in length.
  - Since variable names are not case sensitive, we can write in `camelCase` or `PascalCase` or `snake_case`. We will use camelCase.

  We can store values in variables using `=` equals sign.

  ```javascript
  testVariable = "48";
  ```

  In JS, variable takes on the type of the value we store in it. Let's find the type of `testVariable`

  **Note:** *Since there is no way to get object type from variable, we used Object.prototype.toString.call(variable)*

  ```javascript
    Object.prototype.toString.call(testVariable);
    // result: "[object String]"
  ```

  Let's try different type of value.

  ```javascript
    testVariable = 48;
    Object.prototype.toString.call(testVariable)
    // result: "[object Number]"
  ```

  Example with respect to Selenium

  ```javascript
    var pageTitle = driver.getTitle();
  ```

- **Methods**

  When we group common actions together for reuse, it'll become method.

  Method names follow the same rules as variables.

  **How method differece from variable?**
  - Method name will be a verb (action).
  - We use function call when declaring method.
  - Contents of the method are wrapped in `{` `}` brackets.

  ```javascript
  var test_method = function() {
    // code
  };

  test_method();
  ```

  **Passing an argument.**

  ```javascript
  var test_method = function(message) {
    console.log(message);
  };

  test_method('Learning Javascript');
  // result: Learning Javascript
  ```

  **Passing an argument with default value.**

  ```javascript
  var test_method = function(message = 'Specify message') {
    console.log(message);
  };

  test_method();
  // result: Specify message
  ```

- **Classes**

  It's important to note that there are no classes in JavaScript. But there are functions (which are objects that can contain behavior and state) which can be used to simulate classes. But in general JavaScript is a class-less language. Everything is an object. And when it comes to inheritance, objects inherit from objects, not classes from classes.

  Classes contain variables and methods.

  Classes are in fact *special functions*. So to declare a class we need to specify the keyword `function` followed by the `name`.

  **Naming rules**
  - Should start with capital letter.
  - Should be PascalCase for multiple words.
  - Should be descriptive (a noun).

  Let's create a class.

  ```javascript
  function Messenger() {
    ...
  };
  ```

  Let's add method to created class.

  ```javascript
  Messenger.prototype.say = function(message) {
    console.log(message);
  };
  ```

  Now create an instance of an object to access the created method.

  ```javascript
  var messenger = new Messenger();
  messenger.say('This is an instance of a class');

  // result: This is an instance of a class
  ```

  **Note:** The function block used to declare a class is a method in it's own. It's considered as a *constructor method*. This is a method that gets automatically executed when a new instance of the class is created.

## Scope

## Actions

- **Assertions**
- **Conditionals**

## Inheritance

## Promises

Let's step through each concept and understand how they pertain to test automation. We will use Selenium to interact with Browsers and for examples.
