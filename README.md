<div align="center">

# 🧱 Programming Foundations — C & C++

**The low-level base under my embedded and radar work: memory, pointers, the stack, assembly output, RAII and move semantics.**

![C](https://img.shields.io/badge/C-C99-A8B9CC?logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-17-00599C?logo=cplusplus&logoColor=white)
![CMake](https://img.shields.io/badge/build-CMake%20·%20clang-064F8C?logo=cmake&logoColor=white)

</div>

> **RU:** Основы C и C++ с прицелом на embedded: память, указатели, стек и прерывания, ассемблерный вывод компилятора, RAII, правило пяти.
> **TR:** Gömülü sistemlere yönelik C ve C++ temelleri: bellek, işaretçiler, stack ve ISR, derleyici assembly çıktısı, RAII, Rule of Five.

Merged from my earlier repos `c-foundations`, `cpp-labs` and `ProgC` (git history kept). Compiled binaries were removed from history.

## 🗂️ Contents

| Folder | Topics |
|---|---|
| [`c/basics/`](c/basics) | 14 small programs: lessons 1–7 (types, math, switch, functions, strings), pointers, macros, `goto`/`break`/`continue`, file read/write, bubble sort, memory addresses, random/probability — several with the compiler's `.s` assembly next to the C |
| [`c/firmware/01_stack/`](c/firmware/01_stack) | stack growth, local variable addresses, recursion, stack overflow, ISR design rules |
| [`cpp/memory/`](cpp/memory) | stack vs heap, `sizeof`, array addresses · pointers, references, `const`, `volatile` |
| [`cpp/oop/`](cpp/oop) | RAII for embedded drivers (why copying is forbidden) · Rule of Three / Five and move semantics |
| [`cpp/early_2024/`](cpp/early_2024) | first C++ programs (2024) |

## 🚀 Build

```bash
cd c/basics && cmake -B build && cmake --build build      # or: clang lesson1/main.c -o app
clang -S -O0 lesson1/main.c -o lesson1/main.s              # look at the assembly
clang++ -std=c++17 cpp/oop/01_class_RAII/main.cpp -o raii && ./raii
```

<sub>Where this is used: [embedded-systems-labs](https://github.com/Bugee03/embedded-systems-labs) · see my [profile](https://github.com/Bugee03).</sub>
