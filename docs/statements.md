# Statements

## Variable Declaration

A variable declaration specifies a type and identifier.

```
int x;
float value;
Point p;
```

Variables are stack-allocated and uninitialized at declaration.

## Assignment Statement

Assignment updates the value of a variable or lvalue.

```
x = 10;
array[i] = value;
object.field = 42;
```

The left operand must be an lvalue. The right operand is an expression.

Assignment is a statement, not an expression. `if (x = 5)` is not valid syntax.

## Expression Statement

An expression followed by a semicolon forms a statement.

```
functionCall();
object.method();
```

## Return Statement

The `return` statement exits a function, optionally returning a value.

```
return;           // void return
return 42;        // return with value
return x + y;     // return expression result
```

A function with non-void return type must return a value. A function with void return type must not return a value.

## If Statement

The `if` statement conditionally executes a block of statements.

```
if (condition) {
  // statements
}
```

An optional `else` clause executes when the condition is false.

```
if (condition) {
  // true branch
} else {
  // false branch
}
```

## While Statement

The `while` statement repeatedly executes a block while a condition is true.

```
while (condition) {
  // loop body
}
```

### Break Statement

The `break` statement exits the innermost loop.

```
break;
```

### Continue Statement

The `continue` statement skips to the next iteration of the innermost loop.

```
continue;
```

## Compound Statement

A compound statement is a sequence of statements enclosed in braces.

```
{
  int x;
  x = 10;
  functionCall(x);
}
```

Compound statements introduce a new scope for variable declarations.

## Scope Rules

Variables are scoped to the block in which they are declared. Inner blocks may shadow outer variables with the same name. Variables are visible from their declaration point to the end of the enclosing block.
