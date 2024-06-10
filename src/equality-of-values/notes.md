# Equality of Values

If you don’t have a clear mental model of equality in JavaScript, every day is like a carnival—and not in a good way.

## Kinds of Equality

- Strict Equality: a === b (triple equals).
- Loose Equality: a == b (double equals).
- Same Value Equality: Object.is(a, b).

```js
let dwarves = 7;
let continents = "7";
let worldWonders = 3 + 4;

console.log(Object.is(dwarves, continents)); // false
console.log(Object.is(continents, worldWonders)); // false
console.log(Object.is(worldWonders, dwarves)); // true
```

#### But What About Objects?

```js
let banana = {};
let cherry = banana;
let chocolate = cherry;
cherry = {};

console.log(Object.is(banana, cherry)); // false
console.log(Object.is(cherry, chocolate)); // false
console.log(Object.is(chocolate, banana)); // true
```

### Strict Equality: a === b

`console.log(2 === 2); // true`
`console.log({} === {}); // false`

#### Same Value Equality vs. Strict Equality

- Same value equality—Object.is(a, b)—has a direct meaning in our mental model. It corresponds to the idea of “the same value” in our universe.

#### First Special Case: NaN

```js
let width = 0 / 0; // NaN
let height = width * 2; // NaN

console.log(width === height); // false
console.log(Object.is(width, height)); // true
```

#### Second Special Case: -0

```js
let width = 0; // 0
let height = -width; // -0
console.log(width === height); // true
console.log(Object.is(width, height)); // false
```

#### Coding Exercise

Strict equals function example
https://gist.github.com/gaearon/08a85a33e3d08f3f2ca25fb17bd9d638

### Loose Equality

```js
console.log([[]] == ""); // true
console.log(true == [1]); // true
console.log(false == [0]); // true
```

Common uses

```js
if (x == null) {
  // ...
}

if (x === null || x === undefined) {
  // ...
}
```
