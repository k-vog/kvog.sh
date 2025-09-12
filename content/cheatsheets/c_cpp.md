+++
title = 'C/C++'
+++

* [Preprocessor Definitions](#preprocessor-definitions)
  * [Platform detection](#platform-detection)
  * [Compiler detection](#compiler-detection)
  * [Architecture detection](#architecture-detection)
* [Standard Headers](#standard-headers)

## Preprocessor Definitions

* [predef wiki](https://github.com/cpredef/predef)

### Platform detection
```
#ifdef _WIN32
  // Windows
#endif

#ifdef __APPLE__
  // Apple

  #include <TargetConditionals.h>
  #idef TARGET_OS_OSX
    // macOS
  #elif TARGET_OS_IPHONE
    // Some kind of mobile device
    #if TARGET_OS_MACCATALYST
      // Mac Catalyst - iOS app on macOS
    #elif TARGET_OS_VISION
      // visionOS
    #elif TARGET_OS_TV
      // tvOS
    #else
      // iOS
    #endif
  #endif // TARGET_OS_OSX
#endif // __APPLE__

#ifdef __linux__
  // Linux
#endif

```

### Compiler detection
```
#ifdef __GNUC__
  // GCC
#endif

#ifdef __clang__
  // clang
#endif

#ifdef _MSC_VER
  // Visual C++
#endif
```

### Architecture detection
```
#if (defined(_MSC_VER) && _M_X64) || (defined(__GNUC__) && __amd64__)
  // x86-64
#endif

#if (defined(_MSC_VER) && _M_ARM64) || (defined(__GNUC__) && __aarch64__)
  // arm64
#endif
```

## Standard Headers

* [C standard headers](https://en.cppreference.com/w/c/header.html)
* [C++ standard headers](https://en.cppreference.com/w/cpp/header.html)
#
* [assert.h](https://en.cppreference.com/w/c/header/assert.html)
* [complex.h](https://en.cppreference.com/w/c/header/complex.html)
* [ctype.h](https://en.cppreference.com/w/c/header/ctype.html)
* [errno.h](https://en.cppreference.com/w/c/header/errno.html)
* [fenv.h](https://en.cppreference.com/w/c/header/fenv.html)
* [float.h](https://en.cppreference.com/w/c/header/float.html)
* [inttypes.h](https://en.cppreference.com/w/c/header/inttypes.html)
* [iso646.h](https://en.cppreference.com/w/c/header/iso646.html)
* [limits.h](https://en.cppreference.com/w/c/header/limits.html)
* [locale.h](https://en.cppreference.com/w/c/header/locale.html)
* [math.h](https://en.cppreference.com/w/c/header/math.html)
* [setjmp.h](https://en.cppreference.com/w/c/header/setjmp.html)
* [signal.h](https://en.cppreference.com/w/c/header/signal.html)
* [stdalign.h](https://en.cppreference.com/w/c/header/stdalign.html)
* [stdarg.h](https://en.cppreference.com/w/c/header/stdarg.html)
* [stdatomic.h](https://en.cppreference.com/w/c/header/stdatomic.html)
* [stdbit.h](https://en.cppreference.com/w/c/header/stdbit.html)
* [stdbool.h](https://en.cppreference.com/w/c/header/stdbool.html)
* [stdckdint.h](https://en.cppreference.com/w/c/header/stdckdint.html)
* [stddef.h](https://en.cppreference.com/w/c/header/stddef.html)
* [stdint.h](https://en.cppreference.com/w/c/header/stdint.html)
* [stdio.h](https://en.cppreference.com/w/c/header/stdio.html)
* [stdlib.h](https://en.cppreference.com/w/c/header/stdlib.html)
* [stdmchar.h](https://en.cppreference.com/w/c/header/stdmchar.html)
* [stdnoreturn.h](https://en.cppreference.com/w/c/header/stdnoreturn.html)
* [string.h](https://en.cppreference.com/w/c/header/string.html)
* [tgmath.h](https://en.cppreference.com/w/c/header/tgmath.html)
* [threads.h](https://en.cppreference.com/w/c/header/threads.html)
* [time.h](https://en.cppreference.com/w/c/header/time.html)
* [uchar.h](https://en.cppreference.com/w/c/header/uchar.html)
* [wchar.h](https://en.cppreference.com/w/c/header/wchar.html)
* [wctype.h](https://en.cppreference.com/w/c/header/wctype.html)
