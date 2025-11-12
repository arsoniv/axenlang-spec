# Program Structure

## Compilation Units

A source file is a compilation unit containing declarations. The file extension is `.ax`.

## Import Statement

The `import` statement includes declarations from another source file.

```
import "filename.ax";
```

The filename is specified as a string literal and is resolved relative to the importing file.

### Import Semantics

- Imports are processed at compile time
- All declarations from the imported file become available in the importing file
- Circular imports should be avoided
- Each file is processed once; multiple imports of the same file do not cause duplication

## Entry Points

AxenLang does not require a specific entry point function. Any function may serve as the entry point depending on the linking configuration.

When linking with the C runtime, a function named `main` with the C-compatible signature is used:

```
int main() {
  return 0;
}
```

For standalone executables or custom runtimes, any function can be designated as the entry point.

## Compilation Model

1. The compiler parses the root source file
2. Import statements are resolved and imported files are parsed
3. All declarations are collected across all compilation units
4. Type checking and semantic analysis are performed
5. LLVM IR is generated for all functions
6. The output is an object file or LLVM IR text

## Linking

Generated object files can be linked with:
- C standard library
- Custom runtime libraries
- Other object files from C, C++, or AxenLang

The linking process determines the actual entry point and resolves external symbols.
