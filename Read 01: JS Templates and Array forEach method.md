# READ 01

## Template Literals

- Template literals allow embedded expressions, you can use multi-line strings and string interpolation features with them.
- Template literals are enclosed by the backtick(``).
- Placeholder = ${expression}.

### String interpolation

- is the process of evaluating a string literal containing one or more placeholders, yielding a result in which the placeholders are replaced with their corresponding values.

### String Substitution

- Allows us to take any valid JS expression and put it inside a Template Literal, the result will be output as part of the same string.
  - `Sup ${name.toUpperCase()}, i made $${5 * (a * 8)} last week and ill make $${monthlyIncome()} this month.`.

### HTML TEMPLATES

- much like multi line strings- you can use the backticks to make templates:

function createMarkup(data) {
    return `
        `<article class="pokemon">`
            `<h3>${data.name}</h3>`
            `<p>The Pokemon ${data.name} has a base experience of ${data.base_experience}, they also weigh ${data.weight}</p>`
       ` </article>`
    `
};

### Array.prototype.forEach()

- forEach() executes a provide function once for each array element.

`const array1 = ['a', 'b', 'c'];`

`array1.forEach(element => console.log(element));`

// expected output: "a"
// expected output: "b"
// expected output: "c"

`arr.forEach(callback(currentValue[, index[, array]]) {`
  `// execute something`
`}[, thisArg]);`

**callback** : function to execute on each element, it accepts between one and three arguments:

- ***currentValue*** : The current element being processed in the array. the value of the element.

- ***index***(optional) : the index of*currentValue* in the array. the index of the element.

- ***array***(optional) : The array *forEach()* was called upon. the array object being traversed.

**thisArg**(optional) : Value to use as *this* when executing *callback*.

*Return value =  **undefined***

- the range of element processed by *forEach()* is set before the first invocation of *callback*, elements appended to the array after the call to *forEach()* will not be visited by the *callback*. if existing elements of the array are changed or deleted their value as passed to *callback* will be the value at the time *forEach()* visits them, elements deleted before being visited are not visited. if Elements are removed after being visited (shift()) during the iteration, later elements will be skipped.

- there is no way to stop or break a *forEach()* loop other than throwing an exception. if you need such behavior, *forEach()* is the wrong tool.

- *forEach()* returns undefined and is not chainable. typical use case is to execute side effects at the end of a chain.


### Converting a for loop to forEach

const items = ['item1', 'item2', 'item3']
const copyItems = []

// before
for (let i = 0; i < items.length; i++) {
  copyItems.push(items[i])
}

// after
items.forEach(function(item){
  copyItems.push(item)
})

### For loops vs forEach in JavaScript

- Arrays: use for...of if you don’t care about index value. I like to use forEach for all my iterations though — no refactoring needed if I ever decide I do need the index value.

- Objects: use for...of if you don’t care about key value; Object.keys() if you do (and use obj[key] to get the value).

- Everything: use lodash if it is a possibility. There’s a reason it’s the most downloaded and depended-on library on NPM.
