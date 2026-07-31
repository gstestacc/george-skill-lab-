---
name: my-formatter
description: "Apply my own simple house style to a block of text: a title, a divider, bold callouts, and a signature line. Use when the user pastes text and asks to format it in my personal style, or mentions 'my formatter' or 'my house style'."
---

# My first formatter

This is a practice skill. It restyles text; it does not rewrite the words.

## What this does

Given a block of text from the user, produce a version with:

1. **Title** - take the first line as the title. Format it as a Markdown H1
   (`# Title`).
2. **Divider** - insert `---` directly under the title.
3. **Callouts** - any line starting with `IMPORTANT:` gets wrapped in bold
   (`**IMPORTANT: ...**`). Leave every other line exactly as written.
4. **Signature** - add this line at the very end, on its own line:
   `_Formatted with my-formatter_`
5. **Timestamp** - add today's date on its own line after the signature.

## What this does not do

- Does not correct spelling, grammar, or wording.
- Does not add content the user did not provide.
- Does not touch anything except the four transformations above.

## Example

Input:
```
Project update
Things are on track.
IMPORTANT: budget review is due Friday.
```

Output:
```
# Project update
---
Things are on track.
**IMPORTANT: budget review is due Friday.**

_Formatted with my-formatter_
```
