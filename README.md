# The Ripper Project

Modular, low-level file manipulation libraries that give developers absolute control over their data.

## What is Ripper?

Ripper is a collection of tools for working with a variety of file formats at the lowest possible level. The project provides modular and consistent C++ libraries that together with C bindings offer a platform-independent interface for reading, writing, and manipulating file formats with precision.

Our mantras are:

- **Users must have absolute control over their data.** Use low-level modules to modify and construct files exactly as you want them, or rely on higher-level abstractions to simplify common tasks.
- **The library serializes exactly what you construct.** No hidden validation, no second-guessing your intent. This makes Ripper suitable as a foundation for higher-level tools, validators, and analyzers that _do_ enforce rules.

## Libraries

| Repository                                             | Description                                                                  |
| ------------------------------------------------------ | ---------------------------------------------------------------------------- |
| [io-core](https://github.com/ripper-org/io-core)       | Binary I/O abstractions — reader/writer backends for file and memory streams |
| [pdf-core](https://github.com/ripper-org/pdf-core)     | Low-level PDF manipulation — parsing, creating, and editing PDF documents    |
| [pdf-core-c](https://github.com/ripper-org/pdf-core-c) | C bindings for pdf-core                                                      |

## Design Principles

- **C++23** — Modern standard, no legacy baggage. We strive to use the latest C++ features without compromising portability.
- **C bindings** — Every library exposes a stable C ABI for FFI from any language (Python, Rust, Go, C#, etc.).
- **Opaque pointers** — The C API uses opaque types with accessor functions. Implementation details stay hidden behind a pure C header.
- **Single responsibility** — Each library does one thing well.
