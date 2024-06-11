# Meeting the Primitive Values

### Undefined

- undefined is a blackhole
- there is only one undefined on javascript universe
- undefined !== ReferenceError

### Null

- we can think null as a undefined sister
- the type of null is an object due a javascript bug
- null is used by a intentional missing value

### Booleans

We can perform logical operations with them:

```js
let isSad = true;
let isHappy = !isSad; // The opposite
let isFeeling = isSad || isHappy; // Is at least one of them true?
let isConfusing = isSad && isHappy; // Are both true?
```

### Numbers

JavaScript numbers don’t behave exactly the same way as regular mathematical numbers do. Here is a snippet that demonstrates it:

```js
console.log(0.1 + 0.2 === 0.3); // false
console.log(0.1 + 0.2 === 0.30000000000000004); // true

// floating-point math
```

- JavaScript uses numbers with limited precision.

#### Special Numbers

```js
let scale = 0;
let a = 1 / scale; // Infinity
let b = 0 / scale; // NaN
let c = -a; // -Infinity
let d = 1 / c; // -0
```

### BigInts

Regular numbers can’t represent large integers with precision, so BigInts fill that gap (literally).

```js
let alot = 9007199254740991n; // n at the end makes it a BigInt!
console.log(alot + 1n); // 9007199254740992n
console.log(alot + 2n); // 9007199254740993n
console.log(alot + 3n); // 9007199254740994n
console.log(alot + 4n); // 9007199254740995n
console.log(alot + 5n); // 9007199254740996n
```

- Operations with truly huge numbers may take time and resources
- BigInts were only recently added to JavaScript, so you won’t see them used widely yet and if you use an older browser, they won’t work.

### Strings

All conceivable string values already exist from the beginning—one value for every distinct string

### Symbols

```js
let alohomora = Symbol();
console.log(typeof alohomora); // "symbol"
```

Symbols serve a similar purpose to door keys: they let you hide away some information inside an object and control which parts of the code can access it.
