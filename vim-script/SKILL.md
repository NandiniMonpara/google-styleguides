---
name: google-vim-script
description: Google's official Vim script style guide. Covers plugin structure, naming conventions, portability, and Vimscript best practices.
---

# Google Vim Script Style Guide

> Official Google Vim script coding standards for consistent plugin development.

## Quick Reference

### Golden Rules

1. **Use `scriptencoding utf-8`** — declare encoding
2. **Prefix plugin functions** — avoid namespace collisions
3. **Use `abort` on functions** — fail fast on errors
4. **Check feature availability** — `has('feature')`
5. **Avoid global variables** — use script-local `s:`
6. **Document commands** — help users understand usage
7. **Test on multiple Vim versions** — ensure compatibility

### Naming Conventions (Preview)

| Element | Convention | Example |
|---|---|---|
| Plugin functions | prefix#Function | `myplugin#GetUser` |
| Script-local | s:function | `s:internal_helper` |
| Global variables | g:prefix_variable | `g:myplugin_enabled` |
| Buffer variables | b:variable | `b:current_user` |

## When to Use This Guide

- Writing Vim plugins
- Maintaining Vim configuration
- Code reviews
- Onboarding new contributors

## Full Guide

See [vim-script.md](vim-script.md) for complete details (coming soon).
