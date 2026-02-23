---
name: google-common-lisp
description: Google's official Common Lisp style guide. Covers naming conventions, formatting, macros, documentation, and Lisp best practices.
---

# Google Common Lisp Style Guide

> Official Google Common Lisp coding standards for consistent, maintainable Lisp code.

## Quick Reference

### Golden Rules

1. **Use lowercase with hyphens** — for symbols
2. **Descriptive names** — clarity matters
3. **Document functions** — docstrings for all public functions
4. **Avoid side effects** — prefer pure functions
5. **Use packages** — organize code into namespaces
6. **Macros sparingly** — only when functions won't work
7. **Follow community conventions** — consistency with ecosystem

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Functions | lowercase-with-hyphens | `get-user-by-id` |
| Variables | lowercase-with-hyphens | `user-count` |
| Constants | +surrounded-by-plus+ | `+max-retries+` |
| Globals | *surrounded-by-asterisks* | `*database-connection*` |

## When to Use This Guide

- Writing new Common Lisp code
- Refactoring existing Lisp
- Code reviews
- Onboarding new team members

## Full Guide

See [common-lisp.md](common-lisp.md) for complete details (coming soon).
