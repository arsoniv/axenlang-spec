# Expressions

## Primary Expressions

### Literals

Integer, floating-point, and string literals are primary expressions.

```
42
3.14
"hello"
```

### Identifiers

An identifier referring to a variable or constant is a primary expression.

```
x
count
```

### Parenthesized Expressions

An expression enclosed in parentheses is a primary expression.

```
(x + y)
```

### Function Calls

A function call consists of a function name followed by a parenthesized argument list.

```
functionName(arg1, arg2)
```

## Postfix Expressions

### Array Subscripting

An expression followed by a bracketed index accesses an array element.

```
array[0]
matrix[i][j]
```

### Member Access

The `.` operator accesses a member of a class.

```
point.x
object.field
```

Member access on pointer types automatically dereferences the pointer.

```
ptr.member     // equivalent to ($ptr).member
```

### Method Calls

Methods are called using member access syntax.

```
object.method(args)
```

Methods receive an implicit pointer to the object as the first parameter.

## Prefix Expressions

### Address-Of Operator

The `&` operator produces the address of its operand.

```
&variable
```

The operand must be an lvalue.

### Dereference Operator

The `$` operator dereferences a pointer.

```
$pointer
```

Multiple dereferences may be chained.

```
$$doublePointer
```

### Unary Minus

The `-` operator negates its operand.

```
-x
-42
```

## Binary Expressions

### Arithmetic Operators

```
x + y    addition
x - y    subtraction
x * y    multiplication
x / y    division
x % y    modulo
```

### Comparison Operators

```
x == y   equality
x < y    less than
x > y    greater than
```

### Logical Operators

```
x & y    bitwise AND
```

## Operator Precedence

Operators are evaluated according to the following precedence (highest to lowest):

1. Primary expressions (literals, identifiers, calls, subscripts, member access)
2. Prefix operators (`&`, `$`, `-`)
3. Multiplication, division, modulo (`*`, `/`, `%`)
4. Addition, subtraction (`+`, `-`)
5. Comparison (`<`, `>`)
6. Equality (`==`)
7. Bitwise AND (`&`)

Operators of the same precedence associate left-to-right.

## Type Requirements

Binary arithmetic and comparison operators require operands of the same signedness. Mixing signed and unsigned operands produces a semantic error.

## Evaluation

Expressions are evaluated left-to-right respecting precedence and associativity rules. There are no short-circuit evaluation semantics for logical operators.
