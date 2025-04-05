# [Type Conversion](https://developer.mozilla.org/en-US/docs/Glossary/Type_Conversion)

>Type conversion  means transfer of data from one data type to another. Implicit conversion happens. The source code can also explicitly require a conversion to take place.

## Example

### Numeric to String Conversion

```js
let num = 69;
let str = "The answer is " + String(69);
console.log({str, type: typeof str});
```

 The number `69` is conversed into a string and concatenated with the string `"The answer is "` by the `String()` function explicitly converts.

_The log in console_: `{ str: 'The answer is 69', type: 'string' }`

### String to Numeric Conversion

```js
let str = "69";
let num = Number(str);
console.log({num, type: typeof num});
````

The string “`69`” is conversed into a numeric value using the `Number()` function.

_The log in console_: `{ num: 69, type: 'number' }`

## String to a Boolean Conversion

```js
let boolean = true;
let str = Boolean("false");
console.log(str == boolean);
```

Conversion the string `"false"` into a Boolean that is true which [Truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy) before comparing it with `true`.

_The log in console_: `true`
