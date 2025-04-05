# [Type coercion](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion)

Type conversion (or typecasting) means transfer of data from one data type to another. _Implicit conversion_ happens when the compiler (for compiled languages) or runtime (for script languages like [JavaScript](https://developer.mozilla.org/en-US/docs/Glossary/JavaScript)) automatically converts data types. The source code can also _explicitly_ require a conversion to take place.

## Example

### Numeric to String Coercion

```js
let num = 69;
let str = "The answer is " + num;
console.log({str, type: typeof str});
```

 The number `69` is coerced into a string and concatenated with the string `"The answer is "`.

_The log in console_: `{ str: 'The answer is 69', type: 'string' }`

### String to Numeric Coercion

```js
let str = "69";
let num = +str;
console.log({num, type: typeof num});
````

The string “`69`” is coerced into a numeric value using the unary plus operator.

_The log in console_: `{ num: 69, type: 'number' }`

## Comparison Coercion

```js
let str = "69";
let num = 69;
console.log(str == num);
```

The loose equality operator `==` coerces the string `"42"` into a number before comparing it with the number `42`.

_The log in console_: `true`
