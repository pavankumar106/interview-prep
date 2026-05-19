## 1. Explain difference between var, let and const.

| Feature                       | `var`             | `let`        | `const`       |
| ----------------------------- | ----------------- | ------------ | ------------- |
| Scope                         | Function scoped   | Block scoped | Block scoped  |
| Re-declaration                | Allowed           | Not allowed  | Not allowed   |
| Re-assignment                 | Allowed           | Allowed      | Not allowed   |
| Hoisted                       | Yes               | Yes          | Yes           |
| Accessible before declaration | Yes (`undefined`) | No (TDZ)     | No (TDZ)      |
| Preferred today               | Rarely            | Yes          | Yes (default) |

## 2. what are closures in js and how do you use them

    Closures occur when a function retains access to variables from
    its lexical scope even after the outer function has completed execution.
    They are used for data hiding, callbacks, event handlers, currying,
    and maintaining state.

    Advantages of Closures:

    Data privacy
    State preservation
    Encapsulation
    Functional programming patterns
    Memoization
    Currying

```js
function outer() {
  let count = 0;

  function inner() {
    count++;
    console.log(count);
  }

  return inner;
}

const counter = outer();

counter(); // 1
counter(); // 2
counter(); // 3
```

## 3. how do you handle async code using async/await and promises

    JavaScript handles asynchronous operations using Promises and
    async/await. Promises represent future values and support
    chaining with .then() and .catch(). Async/await is built on top
    of Promises and provides cleaner syntax that looks synchronous.
    I usually use try/catch for error handling and Promise.all() for
    running independent async operations in parallel.

```js
const promise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Data fetched");
  } else {
    reject("Error occurred");
  }
});
```

```js
async function getData() {
  try {
    const response = await fetch("https://api.example.com/users");

    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.log(error);
  }
}
```
