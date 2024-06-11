# Mental Models

```js
// Declare a variable called a. Set it to 10.
let a = 10;

// Declare a variable called b. Set it to a.
let b = a;

// Set the a variable to 0.
a = 0;

// So a is 0 and b is 0
```

- This happens because javascript doest not set the `a` var, js assign the variable.

## Coding, Fast and Slow

The following code duplicates a spreadsheet, but the the codes also has a bug that changes the title of the original file, something that could be unnoticed if we use the "fast" system, and Dan explains that we should use the "slow" system to retrace what the code does step by step.

```js
function duplicateSpreadsheet(original) {
  if (original.hasPendingChanges) {
    throw new Error("You need to save the file before you can duplicate it.");
  }
  let copy = {
    created: Date.now(),
    author: original.author,
    cells: original.cells,
    metadata: original.metadata,
  };
  copy.metadata.title = "Copy of " + original.metadata.title;
  return copy;
}
```
