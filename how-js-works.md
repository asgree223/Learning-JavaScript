# 📘 What I Learned Today – JavaScript Engine & Hoisting

Today I learned how JavaScript works behind the scenes.

##  JavaScript Engine

A JavaScript engine is a program that executes JavaScript code.  
It first compiles the code and then executes it.

### Example engines:
- V8 (Chrome)
- SpiderMonkey (Firefox)

##  Compilation Phases
JavaScript code goes through the following phases:
1. Lexical Analysis (Tokenizing)
2. Parsing (Creating AST – Abstract Syntax Tree)
3. Code Generation

##  Execution Context
JavaScript runs code inside an execution context.
The Global Execution Context has two phases:
- **Creation Phase:** Variables are stored with `undefined`, and functions are stored in memory.
- **Execution Phase:** Code runs line by line.

## Hoisting
Hoisting means variables and function declarations are moved to the top of their scope during the creation phase.
- var is hoisted and initialized with `undefined`
- let and const are hoisted but not initialized (Temporal Dead Zone)

##  Example

```js
console.log(name);
var name = "Asgaree";
Output-->undefined
