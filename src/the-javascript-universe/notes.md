# The JavaScript Universe

What is a value?

- Numbers, string, objects and functions.

Not value

- if statements, loops, and variable declarations.

## Values and Code

!["In our JavaScript universe, values float in space."](./values%20and%20codes.jpg);

Dan likes to imagine our code as a planet, with their if statements, variable declarations and etc. And likes to see our values floating in space.

## Values

There are two kinds of values

### Primitive Values

Primitive values are numbers string, among other things. _They are permanent part of our Javascript universe. I can point to them, but I can't create destroy, or change them._

### Objects and Functions

They are also values but we can manipulate them from my code.

## Types of values

We can break values down into types.

### Primitive values

- Undefined, unintentionally missing values.
- Null, intentionally missing values.
- Booleans, used for logical operators.
- Numbers, math calculations.
- BigInts, math on big numbers.
- Strings, used for text.
- Symbols, performs rituals and hide secrets.

### Objects and Functions

- Objects, group related data and code.
- Functions, refer to code.

### No Other Types

In javascript, there are no other fundamental value types other than the ones we have just enumerated. The rest are all objects!!!

```js
console.log(typeof []); // "object"
console.log(typeof new Date()); // "object"
console.log(typeof /(hello|goodbye)/); // "object"
```

There is a popular urbans legends that everything is an object in JS. Primitive values are not objects.

### Checking a type

We can use the typeof operator to check the value's type.

```js
console.log(typeof 2); // "number"
console.log(typeof "hello"); // "string"
console.log(typeof undefined); // "undefined"

console.log(typeof {}); // "object"
console.log(typeof []); // "object"
console.log(typeof ((x) => x * 2)); // "function"
```

## Expressions

Dan defines expressions as questions that Javascript can answer, Javascript answers expressions in the only way it knows how, with values.

- Expressions always result in a single value.
