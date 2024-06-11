# Properties

```js
let sherlock = {
  surname: "Holmes",
  address: { city: "London" },
};

let john = {
  surname: "Watson",
  address: sherlock.address,
};

john.surname = "Lennon";
john.address.city = "Malibu";

console.log(sherlock.surname); // "Holmes"
console.log(sherlock.address.city); // "Malibu"
console.log(john.surname); // "Lennon"
console.log(john.address.city); // "Malibu"
```

## Properties

```js
let sherlock = {
  surname: "Holmes",
  age: 64,
};
```

!["Sherlock"](./sherlock.jpg)

In our JavaScript universe, both variables and properties act like “wires.”

- properties don’t contain values—they point to them!

### Reading a Property

```js
console.log(sherlock.age); // 64
```

- `sherlock.age` is our old friend, an expression.

### Property Names

- our object can’t have two properties called age.
- Property names are also always case-sensitive!

### Assigning to a Property

```js
sherlock.age = 65;
```

- Note that we don’t follow the age wire to 64. We don’t care what its current value is.

### Missing Properties

```js
let sherlock = { surname: "Holmes", age: 64 };
console.log(sherlock.boat); // ?
```

JavaScript uses a set of rules that looks something like this:

- Figure out the value of the part before the dot (.).
- If that value is null || undefined, throw an error immediately.
- Check whether a property with that name exists on our object:
  a. If it exists, answer with the value this property points to.
  b. If it doesn’t exist, answer with the undefined value.

```js
let sherlock = { surname: "Holmes", age: 64 };
console.log(sherlock.boat); // undefined
console.log(sherlock.boat.name); // TypeError!
```
