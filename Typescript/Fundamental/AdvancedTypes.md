# [Advanced Type Concepts](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html)

## [Unions](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types)

Create flexible types that can be one of several types:

```typescript
type WindowStates = 'open' | 'closed' | 'minimized';
type Result = string | number[];
```

## [Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html)

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
