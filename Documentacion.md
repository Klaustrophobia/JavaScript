## INTRODUCTION

    1. JavaScript is case sensitive.
    2. Instructions are called statements and are separated by semicolons (;).
    3. A semicolon is not necessary after a statement if it is written on its own line. But if more than one statement on a line is         desired, then they must be separated by semicolons.

## DECLARATION

    JavaScript has three kinds of variable declarations.

        var
        Declares a variable, optionally initializing it to a value.

        let
        Declares a block-scoped, local variable, optionally initializing it to a value.

        const
        Declares a block-scoped, read-only named constant.

## VARIABLES

    You use variables as symbolic names for values in your application. The names of variables, called identifiers, conform to certain rules.

    A JavaScript identifier usually starts with a letter, underscore (_), or dollar sign ($). Subsequent characters can also be digits (0 – 9). Because JavaScript is case sensitive, letters include the characters A through Z (uppercase) as well as a through z (lowercase).

    You can declare a variable in two ways:

        With the keyword var. For example, var x = 42. This syntax can be used to declare both local and global variables, depending on the execution context.

        With the keyword const or let. For example, let y = 13. This syntax can be used to declare a block-scope local variable. 

    You can declare variables to unpack values using the destructuring assignment syntax. For example, const { bar } = foo. This will create a variable named bar and assign to it the value corresponding to the key of the same name from our object foo.

    Variables should always be declared before they are used. JavaScript used to allow assigning to undeclared variables, which creates an undeclared global variable. This is an error in strict mode and should be avoided altogether.

    In a statement like let x = 42, the let x part is called a declaration, and the = 42 part is called an initializer. The declaration allows the variable to be accessed later in code without throwing a ReferenceError, while the initializer assigns a value to the variable. In var and let declarations, the initializer is optional. If a variable is declared without an initializer, it is assigned the value undefined.

    const declarations always need an initializer, because they forbid any kind of assignment after declaration, and implicitly initializing it with undefined is likely a programmer mistake.

<table class="standard-table">
  <thead>
    <tr>
      <th scope="row">Variable</th>
      <th scope="col">Explanation</th>
      <th scope="col">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row"><a href="/en-US/docs/Glossary/String">String</a></th>
      <td>
        This is a sequence of text known as a string. To signify that the value
        is a string, enclose it in single or double quote marks.
      </td>
      <td><code>let myVariable = 'Bob';</code> or<br><code>let myVariable = "Bob";</code></td>
    </tr>
    <tr>
      <th scope="row"><a href="/en-US/docs/Glossary/Number">Number</a></th>
      <td>This is a number. Numbers don't have quotes around them.</td>
      <td><code>let myVariable = 10;</code></td>
    </tr>
    <tr>
      <th scope="row"><a href="/en-US/docs/Glossary/Boolean">Boolean</a></th>
      <td>
        This is a True/False value. The words <code>true</code> and
        <code>false</code> are special keywords that don't need quote marks.
      </td>
      <td><code>let myVariable = true;</code></td>
    </tr>
    <tr>
      <th scope="row"><a href="/en-US/docs/Glossary/Array">Array</a></th>
      <td>
        This is a structure that allows you to store multiple values in a single
        reference.
      </td>
      <td>
        <code>let myVariable = [1,'Bob','Steve',10];</code><br>Refer to each
        member of the array like this:<br><code>myVariable[0]</code>,
        <code>myVariable[1]</code>, etc.
      </td>
    </tr>
    <tr>
      <th scope="row"><a href="/en-US/docs/Glossary/Object">Object</a></th>
      <td>
        This can be anything. Everything in JavaScript is an object and can be
        stored in a variable. Keep this in mind as you learn.
      </td>
      <td>
        <code>let myVariable = document.querySelector('h1');</code><br>All of
        the above examples too.
      </td>
    </tr>
  </tbody>
</table>

## Variable scope

    A variable may belong to one of the following scopes:

    Global scope: The default scope for all code running in script mode.
    Module scope: The scope for code running in module mode.
    Function scope: The scope created with a function.

    In addition, variables declared with let or const can belong to an additional scope:

    Block scope: The scope created with a pair of curly braces (a block).

    When you declare a variable outside of any function, it is called a global variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a local variable, because it is available only within that function.

    let and const declarations can also be scoped to the block statement that they are declared in.

    var-declared variables are hoisted, meaning you can refer to the variable anywhere in its scope, even if its declaration isn't reached yet. You can see var declarations as being "lifted" to the top of its function or global scope. However, if you access a variable before it's declared, the value is always undefined, because only its declaration is hoisted, but not its initialization.

## Control Flow
    Control flow in JavaScript refers to the order in which statements are executed in a script. JavaScript provides several control flow statements to direct the flow of your code, including conditionals, loops, and branching statements. Here's an overview of key control flow structures in JavaScript:

### 1. Conditionals:
#### if Statement:
    
    if (condition) {
        // code to be executed if the condition is true
    } else {
        // code to be executed if the condition is false
    }

#### else if Statement:

    if (condition1) {
        // code to be executed if condition1 is true
    } else if (condition2) {
        // code to be executed if condition2 is true
    } else {
        // code to be executed if none of the conditions are true
    }

#### switch Statement:

    switch (expression) {
        case value1:
            // code to be executed if expression matches value1
            break;
        case value2:
            // code to be executed if expression matches value2
            break;
        default:
            // code to be executed if none of the cases match
    }

### 2. Loops:
#### for Loop:

    for (initialization; condition; update) {
        // code to be executed in each iteration
    }
#### while Loop:

    while (condition) {
        // code to be executed as long as the condition is true
    }

#### do...while Loop:

    do {
        // code to be executed at least once and then repeatedly as long as the condition is true
    } while (condition);

#### for...in Loop (Iterating over object properties):

    for (variable in object) {
        // code to be executed for each property in the object
    }

#### for...of Loop (Iterating over iterable objects like arrays):

    for (variable of iterable) {
        // code to be executed for each element in the iterable
    }

### 3. Branching Statements:
    break: Used to terminate a loop or switch statement.

    continue: Skips the rest of the code inside a loop and moves to the next iteration.

    return: Exits a function and optionally returns a value to the caller.
    
    let number = 7;

    if (number > 10) {
        console.log("The number is greater than 10.");
    } else if (number > 5) {
        console.log("The number is greater than 5.");
    } else {
        console.log("The number is 5 or less.");
    }

    for (let i = 0; i < 5; i++) {
        console.log("Iteration " + i);
    }

    let colors = ['red', 'green', 'blue'];
    for (let color of colors) {
        console.log("Color: " + color);
    }
    
    This example includes if statements, a for loop, and a for...of loop. The control flow is determined by the conditions specified in these statements. Understanding and effectively using control flow structures is fundamental to writing structured and meaningful JavaScript code.
        

