# A Beginner's Guide to JavaScript Variables

A variable is a container for storing values in JavaScript and usually assigned to a name for storing values (which can be any JS data type).
It is assigned to a name so that the value it holds can be referenced or accessed through the assigned name.

```js
var myName = 'Lanre';
console.log(myName); //output: Lanre
```

## Creating a Variable

Creating a variable in JavaScript is known as declaring a variable, a variable is declared using certain keywords that have been specialized for declaring variables; `var`, `let`, & `const` and using an (assignment operator `=` ) to assign a value to it as seen in the above example.

## Variable Keywords (`var`, `let` & `const`)

### `var`

The `var` keyword was used to declare variales in the old, pre-ES6 era of JavaScript.

With ES6 (EcmaScript 2015), the beginning of the modern era in JavaScript, the language got two new keywords to help us declare variables. The value of a variable declared by `var` can be reassigned and also re-declared later in the code.

```js
var myName = 'Abass Lanre';
console.log(myName); //output: Abass Lanre
```

Variables declared with `var` can be declared without assigning a value to it, such values will be initialised with a value of `undefined`

### `let`

The `let` keyword was introduced in ES6 (2015) and is used to declare variables in JavaScript.

```js
let myNames = 'Abass Lanre';
console.log(myNames); //output: Abass Lanre
```

The values of the `let` declared variables can be re-assigned but such variables cannot be redeclared, they are also block scoped.

Variables declared with `let` can be declared without assigning a value to it, such values will be initialised with a value of `undefined`; same as `var`

```js
let myNames = 'Abass Lanre';
console.log(myNames); //output: Abass Lanre

let myNames = 'Lanre';
console.log(myNames); //Uncaught SyntaxError: Identifier 'myNames' has already been declared
```

### `const`

The `const` keyword was also introduced in ES6 (2015), and is used to declare variables as well.

```js
const myPermanentName = 'Abdul-Wasi';
console.log(myPermanentName); //output: Abdul-Wasi
```

but the variables declared with `const` cannot be re-declared, re-assigned and cannot be declared without a value assigned to it.

```js
const myPermanentName = 'Abdul-Wasi';
console.log(myPermanentName); //output: Abdul-Wasi
myPermanentName = 'Admin';
console.log(myPermanentName); //output Uncaught TypeError: Assignment to constant variable.
```

### General Rules for Naming Variables

- Variable names cannot start with a number.
- Variable names are case-sensitive.
- Variable names cannot be the same as `js` keywords [Check MDN's keyword documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar)

## The Assignment Operator

An assignment operator assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand.

```js
let me = 'author';
```

That is an assignment expression that assigns the value of 'author' to me.

| Name                      | Shorthand Operator |        Meaning |
| :------------------------ | :----------------: | -------------: |
| Assignment                |      age = 15      |       age = 15 |
| Addition Assignment       |     age += 15      | age = age + 15 |
| Subtraction Assignment    |      age -= 5      |  age = age - 5 |
| Multiplication Assignment |     age \*= 10     | age = age \* 5 |
| Division Assignment       |      age /= 5      |  age = age / 5 |
| Remainder Assignment      |      age %= 2      |  age = age % 2 |

for more visit [mdn's JavaScript Expression and Operators guide.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

### The Increment (++) and Decrement Operator (--)

The inrement (++) and decrement operator (--) adds and subtracts one to & from its `operand` respectively (An `operand` is a quantity on which an operator applies an action to).
These operators only act on one operand, as a result they are called 'unary operators'

They can be used either before or after a variable as prefixes or sufixes;

```js
25++;
22--;
```

or

```js
++25;
--22;
```

When these operators are used as prefixes, JavaScript first adds one to the variable and then returns the value. When used as suffixes, the value is first returned and then the variable is incremented.

## String Interpolation

String interpolation is replacing placeholders with values in a string literal.

The string interpolation in JavaScript is performed by template literals (strings wrapped in backticks `) and \${expression} as a placeholder.

```js
let myName = Abass;

console.log(`My name is ${myName}`); //output: My name is Abass
```

### Template Literals

Template literals are enclosed by the backtick (``) (grave accent) character instead of double or single quotes.

Template literals can contain placeholders. These are indicated by the dollar sign and curly braces `js(${expression})`. The expressions in the placeholders and the text between the backticks (``) get passed to a function.

## Typeof Operator

The `typeof` operator returns a string indicating the data type of its operand.

```js
console.log(typeof 15); //output: number
console.log(typeof 'Abass'); //output: string
console.log(typeof true); //output: boolean
console.log(typeof believe); //output: undefined.
```

**_The last example (console.log(typeof believe);) prints undefined because the variable `believe` is not declared_**

Note: The typeof operator comes before its operand as seen in the examples above.

## Variables Review

- Variables hold reuseable data in a program and associate it with a name.
- Variables are stored in memory.
- `var` keyword is used before ES6 (2015) versions of JavaScript.
- `let` is preferred to declare a variable when it can be reassigned, while `const` is best suited for constant variables.
- The simple assignment operator (=) is used to assign values to variables when declaring variables.
- Template literals use backticks(``) and \${} to interpolate variable values into a string. **_known as sting interpolation_**
- The `typeof` operator returns a string that indicates the data type of its operand.
