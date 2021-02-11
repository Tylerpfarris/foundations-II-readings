# READ 04

## 04.a

### URLSearchParams

- defines utility methods to work with the query string of a URL.

- An object implementing URLSearchParams can directly be used in a for...of structure. ex:

```js
for (const [key, value] of mySearchParams) {}
for (const [key, value] of mySearchParams.entries()) {}
```

**Constructor**: URLSearchParams() returns a URLSearchParams object instance.

**URLSearchParams.toString()**: returns an query string suitable for use in a URL.

### Location

- The Location interface represents the location (URL) of the object it is linked to. Changes done on it are reflected on the object it relates to. Both the Document and Window interface have such a linked Location, accessible via Document.location and Window.location respectively.

### Window: hashchange event

- The hashchange event is fired when the fragment identifier of the URL has changed (the part of the URL beginning with and following the # symbol).

## 04.b

### RegEx

- regular expressions are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern.

- regex is almost universal across programming languages.

- A regular expression is a sequence of characters that define a search pattern.

## 04.c

### Asynchronicity

- Asynchronous means that things can happen independently of the main program flow.

**error-first callbacks** - the first parameter in any callback function is the error object

```js
fs.readFile('/file.json', (err, data) => {
  if (err !== null) {
    //handle error
    console.log(err)
    return
  }

  //no errors, process data
  console.log(data)
})
```

- setTimeout() executes a particular block of code once after a specified time has elapsed.
  - clearTimeout()

- setInterval() the function you pass as the first parameter is executed repeatedly at no less than the number of milliseconds given by the second parameter apart
  - clearInterval()





### promises 

- Once a promise has been called, it will start in pending state. This means that the caller function continues the execution, while it waits for the promise to do its own processing, and give the caller function some feedback.

At this point, the caller function waits for it to either return the promise in a resolved state, or in a rejected state, but the function continues its execution while the promise does it work.

ex.

```js
chooseToppings()
.then(toppings => placeOrder(toppings))
.then(order => collectOrder(order))
.then(pizza => eatPizza(pizza))
.catch(failureCallback);
```

- promise terminology

- When a promise is created, it is neither in a success or failure state. It is said to be pending.
When a promise returns, it is said to be resolved.
A successfully resolved promise is said to be fulfilled. It returns a value, which can be accessed by chaining a .then() block onto the end of the promise chain. The callback function inside the .then() block will contain the promise's return value.
An unsuccessful resolved promise is said to be rejected. It returns a reason, an error message stating why the promise was rejected. This reason can be accessed by chaining a .catch() block onto the end of the promise chain.

### FETCH

- get data from APIs

```js
fetch(API)
    .then(function(response){
    return response.json();
    }).then(function(response){

    })
```

- fetch() creates a promise that resolves with a response object.

- So for every fetch() whose data you want to show or manipulate you will need at least two then() methods: the first to return the response method that retrieves your data, and the second then to actually work with the data.
