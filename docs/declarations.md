# Declarations

## Function Declarations

A function declaration specifies a return type, name, parameter list, and body.

```
returnType functionName(paramType1 param1, paramType2 param2) {
  // function body
}
```

### Parameters

Parameters are declared with type and name. Multiple parameters are separated by commas.

```
int add(int a, int b) {
  return a + b;
}

void process(int x, ptr float data) {
  // implementation
}
```

### Return Type

Functions must declare a return type. Functions returning no value use `void`.

```
void noReturn() {
  // no return statement needed
}

int getValue() {
  return 42;
}
```

## Class Declarations

A class declaration defines an aggregate type with members and methods.

```
class ClassName {
  memberType1 member1;
  memberType2 member2;
}
```

### Members

Class members are typed fields (without any initalised values)

```
class Rectangle {
  int width;
  int height;
}
```

### Methods

Methods are functions associated with a class. They are declared outside the class body with the naming convention `ClassName_methodName`.

```
class Counter {
  int value;
}

void Counter_init(ptr Counter this) {
  this.value = 0;
}

void Counter_increment(ptr Counter this) {
  this.value = this.value + 1;
}

int Counter_getValue(ptr Counter this) {
  return this.value;
}
```

Methods receive a pointer to the instance as the first parameter, conventionally named `this`.

### Method Calls

Methods are invoked using member access syntax on instances.

```
Counter c;
c.init();
c.increment();
int val;
val = c.getValue();
```

The compiler automatically passes the instance address as the first argument.

## Type Definitions

### typedef

The `typedef` keyword creates a type alias.

```
typedef AliasName ExistingType;
```

Examples:

```
typedef Size int;
typedef CharPtr ptr char;
```

### intdef

The `intdef` keyword defines named integer constants.

```
intdef ConstantName value;
```

Examples:

```
intdef MAX_COUNT 100;
intdef BUFFER_SIZE 1024;
```

Named constants defined with `intdef` can be used in expressions wherever integer literals are valid.

## Global Scope

Functions and classes are declared at global scope. Variables cannot be declared at global scope; they must be declared within functions.
