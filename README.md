# AxenLang Specification

Official documentation for the AxenLang programming language.

[![Documentation](https://img.shields.io/badge/docs-mkdocs-blue)](https://arsoniv.github.io/axenlang-spec/)
[![License](https://img.shields.io/badge/license-GPL--3.0-green)](LICENSE)

## About

This repository contains the language specification and documentation for AxenLang, a simple statically-typed programming language with an LLVM backend.

**Compiler Repository**: [arsoniv/axenc](https://github.com/arsoniv/axenc)

## Building Documentation

The documentation is built with [MkDocs](https://www.mkdocs.org/) using the Material theme.

### Prerequisites

```bash
pip install mkdocs mkdocs-material
```

### Local Development

Serve the documentation locally with live reload:

```bash
mkdocs serve
```

Then open http://localhost:8000 in your browser.

### Build Static Site

```bash
mkdocs build
```

The built site will be in the `site/` directory.

## Documentation Structure

- `docs/index.md` - Specification overview
- `docs/lexical.md` - Lexical structure and tokens
- `docs/types.md` - Type system specification
- `docs/expressions.md` - Expression syntax and semantics
- `docs/statements.md` - Statement forms and control flow
- `docs/declarations.md` - Functions, classes, and type definitions
- `docs/program.md` - Program structure and compilation model

## Contributing

Contributions to improve the documentation are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This documentation is part of the AxenLang project and is licensed under the GNU General Public License v3.0.
