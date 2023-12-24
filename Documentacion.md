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

    

