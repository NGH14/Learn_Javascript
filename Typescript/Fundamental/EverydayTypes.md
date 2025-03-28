
# [Everyday Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

- Build-In Primative JavaScript types: `boolean`, `number`, `string`, `null`, `undefined`, `bigInt`, `symbol`
- Additional TypeScript types: `any`, `unknown`, `never`, `void`

## 1. `string`

- Represents textual data
- Immutable sequence of characters
- Can be created using single quotes, double quotes, or backticks

```typescript
let greeting: string = 'Xin Chao';
let name: string = "Nghia";
let template: string = `${greeting}, ${name}!`;
```

## 2. `number`

- Represents numeric values
- Includes integers and floating-point numbers
- Supports multiple numeric representations

```typescript
let integer: number = 69;
let float: number = 4.19;
let binary: number = 0b1010;
let hexadecimal: number = 0xFF;
let exponential: number = 1.4e10;
```

## 3. `boolean`

- Represents logical values
- Can only be `true` or `false`

```typescript
let isActive: boolean = true;
let hasPermission: boolean = false;
```

## 4. `undefined`

- Represents a variable that has been declared but not assigned a value
- Default return value of functions without explicit return

```typescript
let undefinedVar: undefined;
function noReturn() { } /
```

## 5. `null`

- Represents intentional absence of any object value
- Typically used to indicate a deliberate non-value

```typescript
let emptyValue: null = null;
```

## 6. `symbol`

- Represents a unique and immutable primitive value
- Can be used as object property keys

```typescript
let sym1: symbol = Symbol("description");
let sym2: symbol = Symbol("description");
console.log(sym1 === sym2);
```

## 7. `bigint`

- Represents integers of arbitrary precision
- Created by appending `n` to an integer or using `BigInt()`

```typescript
let bigNumber: bigint = 1234567890123456789012345678901234567890n;
let bigIntFunc: bigint = BigInt(Number.MAX_SAFE_INTEGER);
```

