# Lexical Structure

## Character Set

Source files are processed as sequences of Unicode characters encoded in UTF-8.

## Comments

Single-line comments begin with `//` and continue to the end of the line.

```
// This is a comment
```

Single-line comments begin with `/*` and continue to the next `*/`.

```
/* This is a comment */
```

## Identifiers

Identifiers consist of letters and digits. The first character must be a letter.

**Restriction**: Underscores (`_`) are not permitted in identifiers.

```
validName
Name123
```

## Keywords

The following identifiers are reserved as keywords:

```
return    break     continue  if        while     else
ptr       import    class     typedef   intdef
```

## Literals

### Integer Literals

Integer literals may be specified in decimal or hexadecimal notation.

- Decimal: sequence of digits
- Hexadecimal: `0x` or `0X` followed by hexadecimal digits

```
42
0xFF
0x1A2B
```

### Floating-Point Literals

Floating-point literals consist of digits with a decimal point.

```
3.14
0.5
```

### String Literals

String literals are sequences of characters enclosed in double quotes.

```
"hello"
"example string"
```

## Operators and Punctuation

### Arithmetic Operators

```
+    addition
-    subtraction
*    multiplication
/    division
%    modulo
```

### Comparison Operators

```
==   equal to
<    less than
>    greater than
```

### Logical Operators

```
&    bitwise AND (also used for address-of)
```

### Pointer Operators

```
&    address-of
$    dereference
```

### Delimiters

```
(    )    left and right parentheses
{    }    left and right braces
[    ]    left and right brackets
```

### Other Symbols

```
.    member access
,    comma separator
;    statement terminator
=    assignment
```
