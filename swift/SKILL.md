---
name: google-swift
description: Google's official Swift style guide. Covers naming conventions, optionals, protocols, error handling, formatting, and Swift best practices.
---

# Google Swift Style Guide

> Official Google Swift coding standards for consistent, maintainable iOS/macOS code.

## Quick Reference

### Golden Rules

1. **Use Swift naming conventions** — clear, descriptive names
2. **Prefer `let` over `var`** — immutability by default
3. **Use optionals properly** — avoid force unwrapping
4. **Protocol-oriented programming** — prefer protocols over inheritance
5. **Guard for early returns** — reduce nesting
6. **Use type inference** — let Swift infer types when obvious
7. **SwiftLint for consistency** — automate style enforcement

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Types | UpperCamelCase | `UserService` |
| Functions/Methods | lowerCamelCase | `getUserById` |
| Variables/Properties | lowerCamelCase | `userCount` |
| Constants | lowerCamelCase | `maxRetries` |
| Enums | UpperCamelCase | `Direction` |
| Enum cases | lowerCamelCase | `.up`, `.down` |

## When to Use This Guide

- Writing new Swift code
- Refactoring existing Swift
- Code reviews
- Setting up SwiftLint rules
- Onboarding new team members

## Full Guide

See [swift.md](swift.md) for complete details (coming soon).
