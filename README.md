# Nodejs Interview Questions

### 1. What is the callback [(credit to MDN)](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)
A callback (function) is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

Here is a quick example:
```javascript
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}
```
processUserInput(greeting);

### 2. What is the promise [(credit to Eric Elliott)](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)

A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.

It will be in one of 3 possible states:
- **Fulfilled**: onFulfilled() will be called (e.g., resolve() was called)
- **Rejected**: onRejected() will be called (e.g., reject() was called)
- **Pending**: not yet fulfilled or rejected
