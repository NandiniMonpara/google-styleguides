---
name: google-cpp
description: Google's official C++ style guide. Covers headers, naming conventions, formatting, classes, memory management, RAII, smart pointers, and modern C++ features.
---

# Google C++ Style Guide

> Official Google C++ coding standards for consistent, maintainable code.

## Quick Reference

### Golden Rules

1. **Use RAII** — Resource Acquisition Is Initialization
2. **Prefer smart pointers** over raw pointers
3. **Use `const` liberally** — const correctness matters
4. **Avoid manual memory management** — use containers and smart pointers
5. **Follow the Rule of Zero** — let compiler generate special members
6. **Use `nullptr`** instead of `NULL` or `0`
7. **Prefer `auto`** when type is obvious from context

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Files | lower_snake_case | `user_service.cc`, `user_service.h` |
| Classes/Structs | UpperCamelCase | `UserService` |
| Functions | UpperCamelCase | `GetUserById` |
| Variables | lower_snake_case | `user_count` |
| Constants | kUpperCamelCase | `kMaxRetries` |
| Macros | UPPER_SNAKE_CASE | `MAX_BUFFER_SIZE` |

## When to Use This Guide

- Writing new C++ code
- Refactoring existing C++
- Code reviews
- Setting up clang-format rules
- Onboarding new team members

## Full Guide

See [cpp.md](cpp.md) for complete details (coming soon).
