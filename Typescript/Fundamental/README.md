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

## ***[Type Annotation](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)***
>Types can also appear in many more places than just type annotations. As we learn about the types themselves, we’ll also learn about the places where we can refer to these types to form new constructs.

- ***[Everyday Types](EverydayTypes.md)***
- ***[Advanced Types](AdvancedTypes.md)***
