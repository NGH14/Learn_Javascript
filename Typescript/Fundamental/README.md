# [TypeScript from JavaScript](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)

> TypeScript stands in an unusual relationship to JavaScript. TypeScript offers all of JavaScript’s features, and an additional layer on top of these: TypeScript’s type system.

## [Types by Inference](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)

> By understanding how JavaScript works, TypeScript can build a type-system that accepts JavaScript code but has types. This offers a type-system without needing to add extra characters to make types explicit in your code. That’s how TypeScript knows that helloWorld is a string in the above example.

## [Key Benefits](https://www.typescriptlang.org/docs/handbook/2/basic-types.html)

1. **Type Inference**: TypeScript automatically detects and assigns types based on your code.

   ```typescript
   let bestMeal = 'Bun Bo';
   // TypeScript infers this as a string data type
   ```

2. **Explicit Type Definitions**: Explicitly define types using interfaces and type annotations.

   ```typescript
   interface User {
     name: string;
     id: number;
   }

   const user: User = {
     name: 'Nghia',
     id: 0,
   };
   ```

## [Everyday Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

- Build-In Primative JavaScript types: `boolean`, `number`, `string`, `null`, `undefined`, `bigInt`, `symbol`
- Additional TypeScript types: `any`, `unknown`, `never`, `void`

### 1. `string`

- Represents textual data
- Immutable sequence of characters
- Can be created using single quotes, double quotes, or backticks

```typescript
let greeting: string = 'Xin Chao';
let name: string = "Nghia";
let template: string = `${greeting}, ${name}!`;
```

### 2. `number`

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

### 3. `boolean`

- Represents logical values
- Can only be `true` or `false`

```typescript
let isActive: boolean = true;
let hasPermission: boolean = false;
```

### 4. `undefined`

- Represents a variable that has been declared but not assigned a value
- Default return value of functions without explicit return

```typescript
let undefinedVar: undefined;
function noReturn() { } /
```

### 5. `null`

- Represents intentional absence of any object value
- Typically used to indicate a deliberate non-value

```typescript
let emptyValue: null = null;
```

### 6. `symbol`

- Represents a unique and immutable primitive value
- Can be used as object property keys

```typescript
let sym1: symbol = Symbol("description");
let sym2: symbol = Symbol("description");
console.log(sym1 === sym2);
```

### 7. `bigint`

- Represents integers of arbitrary precision
- Created by appending `n` to an integer or using `BigInt()`

```typescript
let bigNumber: bigint = 1234567890123456789012345678901234567890n;
let bigIntFunc: bigint = BigInt(Number.MAX_SAFE_INTEGER);
```

## [Advanced Type Concepts](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html)

### [Unions](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types)

Create flexible types that can be one of several types:

```typescript
type WindowStates = 'open' | 'closed' | 'minimized';
type Result = string | number[];
```

### [Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html)

Add type variables to create reusable, type-safe components:

```typescript
interface Backpack<Type> {
  add: (obj: Type) => void;
  get: () => Type;
}
```

## [Structural Type System](https://medium.com/redox-techblog/structural-typing-in-typescript-4b89f21d6004)

TypeScript uses structural typing, which means objects are considered compatible if they have the same shape:

```typescript
interface Point {
  x: number;
  y: number;
}

function logPoint(p: Point) {
  console.log(`${p.x}, ${p.y}`);
}

const point = { x: 12, y: 26 };
logPoint(point);
```
