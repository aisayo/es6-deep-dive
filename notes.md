# What is ES6

- ECMA stands for European Computer Manufacturing Association
- Puts out guidelines for JavaScript in all browsers
- Ecmascript 6
- “Write less, do more”
- <https://en.wikipedia.org/wiki/ECMAScript>
- <https://www.w3schools.com/js/js_es6.asp>

## ES Evolution

- 1995 — Javascript was created.
- 1997 — ECMAscript 1
- ECMAScript 2–3 are aboned within a few years after ES1, not as important since ES5 eclipsed the other version.
- ES4 — abandoned, sorry.
- 2009 — ES5 is released. Brought forEach, map, and filter to js.
- 2015 — ES6 specs are released
- <https://www.w3schools.com/js/js_versions.asp>

## What did we get from ES6?

### Let and Const

- <https://wesbos.com/let-vs-const>
- <https://medium.com/infancyit/difference-between-var-let-and-const-in-es6-16a08d74b8b2>

#### Const

- Introduced in es6
- Can not be reassigned
- It is immutable except for when used with objects
- Is not hoisted
- Is block scoped
- Always start at const

#### Let

- The new var!
- Mutable
- Can be reassigned and take a new value
- Cannot be redeclared
- Allows for block scoping
- Use let when you know you’re going to re-assign
- <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let>

## Dont use var in production code!!

### Arrow Functions

- Makes code more readable
- If one line, can omit return keyword
- Can use with map, filter, reduce
- Does not have `this`
- Not useful for defining object methods
- Must be defined before they are used, do not get hoisted

### Array and Object Destructuring

#### Destructuring Objects:

- Variables need to match property name
- Can rename variable with (:)
- `const doggie = {
    first: 'Buzz',
    breed: 'Great Pyrenees',
    fur_color: 'black and white',
    activity_level: 'sloth-like',
    favorite_food: 'hot_dogs'
    };`
- `const { first, breed } = doggie;`

##### Nested objects

- `const doggie = {
 first: 'Buzz',
 breed: 'Great Pyrenees',
 fur_color: 'black and white',
 activity_level: 'sloth-like',
 favorite_foods: {
   meats:{
     ham: 'smoked',
     hot_dog: 'oscar_meyer',
   },
   cheeses:{
     american: 'kraft'
   }
 }
};`
- `const { ham, hot_dog } = doggie.favorite_foods.meats;`

#### Destructuring Arrays:

- `const dogs = ['Great Pyrenees', 'Pug', 'Bull Mastiff']
    const [medium, small, giant] = dogs`
- `const dogsName = 'Sir Woody BarksALot'
    const [title, firstName, lastName] = 'Sir Woody BarksALot'.split(' ')`

#### Template Literals

- Use variable inside a string
- Use instead of concatenate

#### Default Parameters

- JavaScript did not have the ability to give default values to parameters
- Pass in a default value to an argument so that undefined will not be returned

#### Rest Parameters

- Ability to pass in an arbitrary number of arguments
- Allows you to collect the rest of your remaining parameters that you are passing into your function into an array

#### Spread Operator

- allows you to pass elements of an array into a function as an argument

#### Classes

- Object Oriented Programming
- Make code more secure and encapsulated
- Use class keyword
- Has a constructor function to add properties
- Type of a function, just uses class keyword

#### Object.assign()

- Non destructive
- Allows us to combine properties from multiple objects into a single object
- First argument is the object we are adding all the properties to
- The next arguments are any objects whose properties we want to add
- Passing in an empty object creates an entirely new object
- Get better performance from merging objects nondestructively
- <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign>
- <https://www.freecodecamp.org/news/javascript-standard-objects-assign-values-hasownproperty-and-getownpropertynames-methods-explained>

#### Promise

- Representation of resolution or rejection asynchronous actions, returning its resulting value
- It is an object
- Will produce a single value in the near future
- ES6 is when Promise global came about
- ES6 promise constructor takes a function. That function takes two parameters, `resolve()`, and `reject()`
- Has 3 states: `pending`, `fulfilled`, `rejected`
- `Promise.prototype.then()` <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then>
- `Promise.prototype.catch()` <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/catch>
- <https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261>
