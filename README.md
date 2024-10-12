# Bella Programming Language Extension

This repository contains an assignment focusing on denotational and operational semantics for a small extension of the Bella programming language, which introduces arrays, booleans, lists, and additional features such as type annotations and tuple types.

## Abstract Syntax

The following abstract syntax defines the language extension:

### Expressions
- n: Numeral
- i: Identifier
- e: Expression
  - n
  - i
  - true
  - false
  - uop e (unary operators: - and !)
  - e1 bop e2 (binary operators: +, -, , /, %, *, <, <=, ==, !=, >=, >, &&, ||)
  - i e* (function calls)
  - e ? e1 : e2 (conditional expressions)
  - [e*] (array literals)
  - e[e] (subscript expressions)

### Statements
- s: Statement
  - let i = e
  - func i i* = e
  - i = e
  - print e
  - while e b

### Blocks and Programs
- b: Block
  - block s*
- p: Program
  - program b

### Additional Features
- Type annotations on variable declarations.
- Tuple types.

## Static Semantics

This section provides the operational static semantics for the Bella extension. Each variable and function should be properly typed according to the language rules. Type checking should ensure that:

1. Variables are declared with type annotations.
2. Function calls have matching argument types.
3. Expressions are type-checked before evaluation, ensuring consistency with declared types.

## Interpreter Implementation

An interpreter for the Bella programming language extension is implemented in TypeScript. The interpreter can handle the defined expressions and statements, including:

- Numerical and boolean literals.
- Function declarations and calls.
- Array and subscript expressions.
- Conditionals and print statements.

### Sample Invocation

To run the interpreter, use the following sample code:

```typescript
const sample: Program = new Program(
  new Block([new PrintStatement(new Numeral(5))])
);

interpret(sample);

Setup Instructions

To set up the project, follow these steps:

	1.	Initialize Node Package Manager

npm init


	2.	Changes in package.json
Update your package.json to include:

{
  "type": "module",
  "main": "bella.js"
}


	3.	Initialize TypeScript Configuration

tsc --init


	4.	Changes in tsconfig.json
Update your tsconfig.json to include:

{
  "compilerOptions": {
    "target": "esnext",
    "module": "esnext"
  }
}


	5.	Compile TypeScript to JavaScript
Use the following command to compile TypeScript files:

tsc --watch  # Compiles bella.ts to bella.js


	6.	Run the Interpreter
After compiling, run the interpreter with:

node bella.js  # OUTPUT

## Usage

To use this repository:

	1.	Clone the repository to your local machine.
	2.	Install the necessary dependencies (if applicable).
	3.	Run the interpreter with your desired Bella program representation.
