# TypeScript Basics Cheatsheet

## Variables and Data Types

```typescript
// Variable declarations
type MyType = string | number;
let variable: MyType = "value";
const constant: number = 42;

// Basic types
let str: string = "text";
let num: number = 123;
let bool: boolean = true;
let arr: number[] = [1, 2, 3];
let tuple: [string, number] = ["hello", 5];
let anyValue: any = "anything";
let unknownValue: unknown = 10;
let neverValue: never;
let obj: { key: string; value: number } = { key: "a", value: 1 };

// Enums
enum Color {
  Red,
  Green,
  Blue
}
let c: Color = Color.Green;
```

## Functions

```typescript
function add(a: number, b: number): number {
  return a + b;
}

const multiply = (a: number, b: number): number => a * b;

// Optional and default parameters
function greet(name: string = "World"): string {
  return `Hello, ${name}!`;
}
```

## Interfaces and Types

```typescript
interface Person {
  name: string;
  age: number;
}

const user: Person = { name: "Alice", age: 30 };

type Point = { x: number; y: number };
const pt: Point = { x: 1, y: 2 };
```

## Classes

```typescript
class Animal {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  speak(): void {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  speak(): void {
    console.log(`${this.name} barks.`);
  }
}
```

## Generics

```typescript
function identity<T>(arg: T): T {
  return arg;
}

let output = identity<string>("myString");
```

## Type Assertions

```typescript
let someValue: any = "this is a string";
let strLength: number = (someValue as string).length;
```

## Modules

```typescript
// Exporting
export function foo() {}
// Importing
import { foo } from "./foo";
```

## Error Handling

```typescript
try {
  // code that may throw
} catch (error) {
  console.error(error);
}
```
