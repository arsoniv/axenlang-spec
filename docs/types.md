# Types

## Primitive Types

### Void Type

```
void
```

Represents absence of a value. Used as function return type for functions that do not return a value.

### Boolean Type

```
bool
```

Represents boolean values.

### Integer Types

Integer types may be signed or unsigned. Signed types are prefixed without `u`, unsigned types with `u`.

```
char     uchar    8-bit
short    ushort   16-bit
int      uint     32-bit
long     ulong    64-bit
```

### Floating-Point Types

Floating-point types are always signed.

```
half     16-bit
float    32-bit
double   64-bit
quad     128-bit
```

## Derived Types

### Pointer Types

A pointer type is formed by applying `ptr` to a base type.

```
ptr int        // pointer to int
ptr ptr char   // pointer to pointer to char
```

### Array Types

An array type specifies a fixed-size sequence of elements of a given type.

```
int[10]       // array of 10 integers
float[5]      // array of 5 floats
```

Arrays can be multi-dimensional:

```
int[3][4]     // 3x4 array of integers
```

### Class Types

Classes define aggregate types with named members.

```
class Point {
  int x;
  int y;
}
```

Classes are value types and are passed by value unless explicitly converted to pointers.

## Type Aliases

Type aliases create alternative names for existing types.

### typedef

Creates an alias for a type.

```
typedef MyInt int;
typedef PointPtr ptr Point;
```

### intdef

Defines named integer constants.

```
intdef MAX_SIZE 100;
```

## Type Compatibility

Types are compatible if they are identical. Integer operations require operands of the same signedness. Type conversions occur implicitly when:

- Converting between integer types of different widths (sign/zero extension or truncation)
- Integer to floating-point conversion

Pointer types are only compatible with other pointer types pointing to the same base type.
