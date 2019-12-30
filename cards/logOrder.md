In what order will the numbers 1-4 be logged to the console when the code below is executed? Why?

```js
(function() {
    console.log(1); 
    setTimeout(function(){console.log(2)}, 1000); 
    setTimeout(function(){console.log(3)}, 0); 
    console.log(4);
})();
```

---
```js
// 1
// 4
// 3
// 2
```

Because of how JavaScript handles asynchronous code like this. The JS runtime is single threaded, so it uses the setTimeout provided by the browser, which then flows code to be executed through the task queue. The JS event loop only moves items from the task queue to the call stack when the call stack is empty, hence the two setTimeout calls happening last.
