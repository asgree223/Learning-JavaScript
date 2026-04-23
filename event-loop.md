# Event Loop in JavaScript ##
JavaScript is a single-threaded language, which means it can do only one task at a time.

## What is Event Loop? ##
The event loop is like a gatekeeper. It continuously checks if the call stack is empty.  
If the call stack is empty, it takes tasks from the callback queue and moves them to the call stack for execution.

## How it works:
- JavaScript uses a Call Stack to execute functions.
- Web APIs handle async tasks like setTimeout, fetch, etc.
- Callback Queue stores completed async tasks.
- The Event Loop checks if the Call Stack is empty.
- If empty, it pushes tasks from the queue to the stack.

## Example:
```js
console.log("Start");

setTimeout(() => {
  console.log("Async Task");
}, 0);

console.log("End");

output-->start
         End
         Async task
