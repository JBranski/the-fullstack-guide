# Promises

## Creating a promise

```jsx 
const newPromise = new Promise(( resolve, reject ) => {
  // ASYNC code goes in here
});
```

### resolve()

`resolve()` can be used to pass information into the `then()` method if the promise is successful.

```jsx
const p1 = new Promise((resolve, reject) => {
  console.log('Running the asynchronous code here');
  const duration =   Math.floor(Math.random() * 5000);
  setTimeout(() => {
    console.log('About to resolve');
    resolve(42); // succeed with a value
  }, duration);
});

p1.then(value => { // notice the value parameter here
  console.log('The promise completed successfully with the following value:');
  console.log(value);
}).catch(err => {
  console.log('The promise has failed with the following message:');
  console.log(err);
});
```

### reject()

`reject()` can be used to pass information into the `catch()` method should the promise fail.

```jsx
 const p1 = new Promise((resolve, reject) => {
  console.log('Running the asynchronous code here');
  const duration =   Math.floor(Math.random() * 5000);
  setTimeout(() => {
    console.log('About to fail');
    reject('Error 42: Life has no meaning'); // fail with a message
  }, duration);
});

p1.then(() => {
  console.log('The promise completed successfully');
}).catch(err => { // notice the err parameter here
  console.log('The promise has failed with the following message:');
  console.log(err);
});
```
