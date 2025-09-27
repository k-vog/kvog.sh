+++
title = 'C/C++'
+++

* [Preprocessor Definitions](#preprocessor-definitions)
  * [Platform detection](#platform-detection)
  * [Compiler detection](#compiler-detection)
  * [Architecture detection](#architecture-detection)
  * [GCC pragmas](#gcc-pragmas)
  * [MSVC pragmas](#msvc-pragmas)
* [Standard Headers](#standard-headers)

## Preprocessor Definitions

* [predef wiki](https://github.com/cpredef/predef)

### Platform detection
```c
#ifdef _WIN32
  // Windows
#endif

#ifdef __APPLE__
  // Apple - flags for specific devices defined in <TargetConditionals.h>
#endif

#ifdef __linux__
  // Linux
#endif

```

### Compiler detection
```c
#ifdef __GNUC__
  // GCC
#endif

#ifdef __clang__
  // clang
#endif

#ifdef _MSC_VER
  // Visual C
#endif
```

### Architecture detection
```c
#if (defined(_MSC_VER) && _M_X64) || (defined(__GNUC__) && __amd64__)
  // x86-64
#endif

#if (defined(_MSC_VER) && _M_ARM64) || (defined(__GNUC__) && __aarch64__)
  // arm64
#endif
```

### GCC pragmas
```c
// Push/pop warning state
#pragma GCC diagnostic push
#pragma GCC diagnostic pop

// Disable a warning
#pragma GCC diagnostic ignored "-Wunused-variable"
```

### MSVC pragmas
```c
// Link against abc.lib
#pragma comment(lib, "abc.lib")

// Push/pop warning state
#pragma warning(push)
#pragma warning(pop)

// Disable a warning
#pragma warning(disable: 4996)
```

## Standard Headers

* [C standard headers](https://en.cppreference.com/w/c/header.html)
* [C++ standard headers](https://en.cppreference.com/w/cpp/header.html)
