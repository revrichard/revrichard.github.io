---
layout: post
title: Vim Cheat Sheet for Markdown Editing
date: 2025-04-20
---

I find cheatsheets very useful when I'm learning, so I made this one for Vim.

##  Essential Modes

| Mode        | Key             | Use                                 |
|-------------|-----------------|--------------------------------------|
| Normal      | `Esc`           | Navigate and edit                   |
| Insert      | `i`, `a`, `o`   | Write text                          |
| Visual      | `v`, `V`        | Select text                         |
| Command     | `:`             | Save, open files, run commands      |

##  Common Markdown Text Actions

| Command           | Use                                             |
|-------------------|--------------------------------------------------|
| `i`, `a`          | Insert before/after cursor                      |
| `o`, `O`          | New line below/above (great for lists/paras)    |
| `>>`, `<<`        | Indent / Un-indent (useful for lists or blocks) |
| `gwip`            | Reflow paragraph (great for tidy line wrapping) |
| `gqap`            | Format paragraph (text width from `:set tw=80`) |
| `:set tw=80`      | Set wrap width (for `gq` formatting)            |

##  Movement for Markdown

| Command    | Use                                               |
|------------|---------------------------------------------------|
| `}` / `{`  | Move forward/backward by paragraph (blank line)   |
| `]]` / `[[`| Jump to next/previous heading                     |
| `*` / `#`  | Move to list bullet / heading (via search)        |
| `H` `M` `L`| Top, Middle, Bottom of screen                     |
| `Ctrl-d/u` | Scroll half page down/up                          |

##  Markdown Formatting Helpers

| Task                   | Command or Insert                      |
|------------------------|----------------------------------------|
| Heading                | `## ` or `### ` (Insert mode)          |
| Bold                   | `**bold**` or `__bold__`               |
| Italic                 | `*italic*` or `_italic_`               |
| Code (inline)          | `` `code` ``                           |
| Code block             | ```` ```lang ↵ code ``` ````          |
| Blockquote             | `> ` at beginning of line              |
| Bullet list            | `- ` or `* ` or `+ `                   |
| Numbered list          | `1. ` etc.                             |
| Checkbox list          | `- [ ] task` / `- [x] done`            |
| Horizontal rule        | `---` or `***`                         |
| Link                   | `[text](url)`                          |
| Image                  | `![alt](path)`                         |

##  Navigation & Search

| Command     | Use                                |
|-------------|------------------------------------|
| `/pattern`  | Search forward                     |
| `n` / `N`   | Next / previous match              |
| `:%s/foo/bar/g` | Replace all `foo` with `bar`   |
| `:noh`      | Clear search highlights            |


