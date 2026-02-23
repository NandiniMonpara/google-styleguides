---
name: google-go
description: Google's official Go style guide. Covers gofmt formatting, naming conventions, error handling, interfaces, concurrency patterns, and package organization. Enforces idiomatic Go code with short variable names and explicit error checks.
---

# Google Go Style Guide

> Official Google Go coding standards for idiomatic, maintainable code.

## Golden Rules

1. **Run `gofmt` before commit** — formatting is non-negotiable
2. **Short variable names** in small scopes — `i`, `err`, `ctx`
3. **Error handling, not exceptions** — check every error
4. **Interfaces for abstraction** — accept interfaces, return structs
5. **Defer for cleanup** — ensure resources are released
6. **Explicit is better** — avoid magic, prefer clarity
7. **Package names: lowercase, single word** — no underscores

## Quick Reference

### Naming Conventions

| Element | Convention | Example |
|---|---|---|
| Packages | lowercase | `package user` |
| Files | lowercase_underscore | `user_service.go` |
| Types | UpperCamelCase | `UserService` |
| Functions/Methods | UpperCamelCase (exported) | `GetUser` |
| Functions/Methods | lowerCamelCase (unexported) | `getUserByID` |
| Variables | lowerCamelCase | `userCount` |
| Constants | UpperCamelCase or UPPER_SNAKE | `MaxRetries` |
| Interfaces | UpperCamelCase + -er suffix | `Reader`, `Writer` |

### Variables

```go
// ✓ CORRECT - short names in small scopes
for i := 0; i < 10; i++ {
    // ...
}

// ✓ CORRECT - descriptive names in larger scopes
func ProcessUserData(userRepository UserRepository) error {
    // ...
}

// ✗ INCORRECT - unnecessarily long
for index := 0; index < 10; index++ {
    // ...
}
```

### Error Handling

```go
// ✓ CORRECT - check every error
user, err := getUser(id)
if err != nil {
    return nil, fmt.Errorf("failed to get user: %w", err)
}

// ✗ INCORRECT - ignoring errors
user, _ := getUser(id)
```

### Functions

```go
// ✓ CORRECT - multiple return values
func GetUser(id int) (*User, error) {
    // ...
}

// ✓ CORRECT - named return values for clarity
func ParseConfig(path string) (cfg *Config, err error) {
    // ...
}
```

### Interfaces

```go
// ✓ CORRECT - small, focused interfaces
type Reader interface {
    Read(p []byte) (n int, err error)
}

// ✓ CORRECT - accept interfaces, return structs
func ProcessData(r Reader) (*Result, error) {
    // ...
}
```

### Defer

```go
// ✓ CORRECT - defer for cleanup
func ReadFile(path string) ([]byte, error) {
    f, err := os.Open(path)
    if err != nil {
        return nil, err
    }
    defer f.Close()
    
    return io.ReadAll(f)
}
```

### Goroutines and Channels

```go
// ✓ CORRECT - use context for cancellation
func ProcessItems(ctx context.Context, items []Item) error {
    for _, item := range items {
        select {
        case <-ctx.Done():
            return ctx.Err()
        default:
            if err := process(item); err != nil {
                return err
            }
        }
    }
    return nil
}

// ✓ CORRECT - buffered channels when appropriate
results := make(chan Result, len(items))
```

### Package Organization

```go
// ✓ CORRECT - package comment
// Package user provides user management functionality.
package user

// ✓ CORRECT - group imports
import (
    "context"
    "fmt"
    
    "github.com/pkg/errors"
    
    "myapp/internal/db"
)
```

## Common Mistakes

| Mistake | Correct Approach |
|---|---|
| Ignoring errors | Check every error |
| Long variable names in loops | Use short names (`i`, `j`) |
| Panic for normal errors | Return errors |
| Naked returns | Use explicit returns |
| Not running gofmt | Always format code |
| Underscores in package names | Use single lowercase word |

## When to Use This Guide

- Writing new Go code
- Refactoring existing Go
- Code reviews
- Setting up linting rules (golangci-lint)
- Onboarding new team members

## Full Guide

See [go.md](go.md) for complete details, examples, and edge cases.
