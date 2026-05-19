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
