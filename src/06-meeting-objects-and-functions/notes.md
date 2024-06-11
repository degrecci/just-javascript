# Meeting Objects and Functions

### Objects

```js
console.log(typeof {}); // "object"
console.log(typeof []); // "object"
console.log(typeof new Date()); // "object"
console.log(typeof /\d+/); // "object"
console.log(typeof Math); // "object"
```

We can access by `.` or `[]` brackets

```js
let rapper = { name: "Malicious" };
rapper.name = "Malice"; // Dot notation
rapper["name"] = "No Malice"; // Bracket notation
```

#### Do Objects Disappear?

- JavaScript doesn’t offer guarantees about when garbage collection happens.
- We can create objects—but we cannot destroy them.

### Functions

#### Functions are Values

```js
for (let i = 0; i < 7; i++) {
  console.log(2);
}
```

How many different values does it pass to console.log?
**one value**

```js
for (let i = 0; i < 7; i++) {
  console.log({});
}
```

How many different values does it pass to console.log now?
**seven values**

```js
for (let i = 0; i < 7; i++) {
  console.log(function () {});
}
```

How many different values does this code pass to console.log?
**seven**
