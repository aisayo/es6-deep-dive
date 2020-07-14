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

`const doggie = {
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
`const { ham, hot_dog } = doggie.favorite_foods.meats;`

#### Destructuring Arrays:

- `const dogs = ['Great Pyrenees', 'Pug', 'Bull Mastiff']
    const [medium, small, giant] = dogs`
- `const dogsName = 'Sir Woody BarksALot'
    const [title, firstName, lastName] = 'Sir Woody BarksALot'.split(' ')`
