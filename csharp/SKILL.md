---
name: google-csharp
description: Google's official C# style guide. Covers naming conventions, formatting, LINQ, async/await, XML documentation, and .NET best practices.
---

# Google C# Style Guide

> Official Google C# coding standards for consistent, maintainable code.

## Quick Reference

### Golden Rules

1. **Follow .NET naming conventions** — PascalCase for public members
2. **Use async/await** for asynchronous operations
3. **LINQ for collections** — prefer declarative over imperative
4. **XML documentation** for public APIs
5. **Use `var`** when type is obvious from right side
6. **Prefer expression-bodied members** when concise
7. **Use nullable reference types** (C# 8.0+)

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Classes/Interfaces | PascalCase | `UserService`, `IRepository` |
| Methods | PascalCase | `GetUserById` |
| Properties | PascalCase | `UserCount` |
| Local variables | camelCase | `userCount` |
| Constants | PascalCase | `MaxRetries` |
| Private fields | _camelCase | `_userId` |

## When to Use This Guide

- Writing new C# code
- Refactoring existing C#
- Code reviews
- Setting up .editorconfig rules
- Onboarding new team members

## Full Guide

See [csharp.md](csharp.md) for complete details (coming soon).
