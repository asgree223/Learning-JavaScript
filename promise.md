# Promises in JavaScript

A Promise is an object that represents the result of an asynchronous operation.

## Why do we use Promises?
Promises help us handle asynchronous tasks more easily and avoid callback hell.

## States of a Promise:
A promise has three states:
- Pending: Initial state, neither fulfilled nor rejected
- Fulfilled: Operation completed successfully
- Rejected: Operation failed

## Example:
```js
const myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Task completed");
  } else {
    reject("Task failed");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
  output--> Task completed
