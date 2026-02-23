---
name: google-objective-c
description: Google's official Objective-C style guide. Covers naming conventions, formatting, memory management, protocols, categories, and Objective-C best practices.
---

# Google Objective-C Style Guide

> Official Google Objective-C coding standards for consistent iOS/macOS code.

## Quick Reference

### Golden Rules

1. **Use ARC** — Automatic Reference Counting
2. **Descriptive naming** — clarity over brevity
3. **Prefix class names** — avoid namespace collisions
4. **Use properties** — prefer @property over instance variables
5. **Nullability annotations** — mark nullable/nonnull
6. **Use modern Objective-C** — literals, subscripting, generics
7. **Follow Apple conventions** — consistency with Cocoa

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Classes | PrefixUpperCamelCase | `GTMUserService` |
| Methods | lowerCamelCase | `getUserById:` |
| Properties | lowerCamelCase | `userCount` |
| Constants | kPrefixUpperCamelCase | `kGTMMaxRetries` |
| Enums | PrefixUpperCamelCase | `GTMDirection` |

## When to Use This Guide

- Writing new Objective-C code
- Maintaining legacy Objective-C
- Code reviews
- Onboarding new team members

## Full Guide

See [objective-c.md](objective-c.md) for complete details (coming soon).
