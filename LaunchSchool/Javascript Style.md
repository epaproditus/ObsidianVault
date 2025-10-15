# JavaScript Style

The JavaScript language has specific stylistic conventions that make reading and writing JavaScript code easier for everyone. You should adopt the styles described in this assignment as quickly as possible. Otherwise, your code may stand out like a sore thumb.

- Your text editor should use two spaces for tabs and indenting should be set to use spaces. You should have done this already back in the previous course. If you don't do it, other people may have problems reading your code.
    
- A sequence of two slashes (e.g., `//`) marks the beginning of a **comment**. Programmers use comments to leave notes for other programmers or themselves. For instance, in the following code:
    
    Copy Code
    
    ```js
    if (isNegativeNumber(value)) {
      return false; // We don't know how to handle negative numbers
    }
    ```
    
    `We don't know how to handle negative numbers` is a comment. The comment has no effect on how the program behaves. It is present merely to provide information to programmers who work on this code.
    
- JavaScript also supports **multi-line comments**. A multi-line comment starts with a `/*` sequence and ends when it finds a `*/` sequence. It's common to include one or two `*` characters at the beginning of each line between the `/*` and `*/` sequences. For instance:
    
    Copy Code
    
    ```js
    /*
    ** This is a multi-line comment. I'm at a loss for words, so I'm just
    ** going to write some nonsense. Dig it?
    */
    ```
    
    The term "multi-line comment" is a bit of a misnomer since, oddly enough, one can be placed entirely on a single line:
    
    Copy Code
    
    ```js
    if (isNegativeNumber(value)) {
      return false; /* We don't know how to handle negative numbers */
    }
    ```
    
    Multi-line comments may even appear in the middle of a line, but that's usually seen as poor style.
    
- When you create a function, method, or variable names, you should usually use **camelCase** formatting: camelCase names always begin with a lowercase letter. Subsequent letters should also be lowercase unless they start a new word. The first letter of each word except the first should be uppercase:
    
    Copy Code
    
    ```js
    // Assigning a variable
    let fourAndTwentyBlackBirds = 24;
    
    // Defining a function
    function thisIsAGreatMethod() {
      // Do some stuff
    }
    ```
    
- File names typically use **snake_case** or **kebab-case**: all lowercase letters with individual words separated with underscores (`_`) or hyphens (`-`):
    
    Copy Code
    
    ```plaintext
    hello_world.js  # snake_case
    hello-world.js  # kebab-case
    ```
    
    Be kind to other people who have to maintain your project: don't mix _snake_case_ and _kebab-case_ names in the same project.
    
- When you want to represent a value that won't change once your program begins running, you can define a constant. In JavaScript, constants often use **PascalCase** (also called **CamelCase** -- the first letter is capitalized) or **SCREAMING_SNAKE_CASE**:
    
    Copy Code
    
    ```js
    const SecondsPerMinute = 60;   // PascalCase (aka CamelCase)
    const SECONDS_PER_MINUTE = 60; // SCREAMING_SNAKE_CASE
    ```
    

One convention that you may encounter is to use SCREAMING_SNAKE_CASE for global, module, or class constants, and CamelCase for local constants inside of functions and methods. Another more-widely accepted convention is to use PascalCase for object type names and constructor functions, such as `Number`, `String`, and `TodoList`. You'll learn more about all these different kinds of named things later.

That about covers the most important style conventions you need to learn during this course. You'll learn more about style issues in the core curriculum. In the meantime, feel free to check the [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript). It's quite long, but it's worth looking it over and reviewing it now and again as you learn more about JavaScript.