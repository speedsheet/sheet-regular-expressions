# Contributing to Regular Expressions SpeedSheet

Thanks for considering a contribution! This speedsheet is community-maintained and we welcome improvements from regex enthusiasts of all experience levels.

## What We're Looking For

**High-value contributions:**
- Missing regex syntax or operators
- Clearer examples for complex patterns (lookahead, backreferences, etc.)
- Common real-world patterns and use cases
- Corrections of errors or outdated information
- Flavor-specific syntax notes (PCRE, JavaScript, Python, etc.)

**Quick wins:**
- Typo fixes
- Broken links
- Pattern improvements
- Better explanations

## Before You Start

1. **Check existing content** - Search the `.stash` file to avoid duplicates
2. **Read the guidelines** - https://speedsheet.io/s/speedsheet_guidelines
3. **Learn Stash format** - https://speedsheet.io/s/stash (simpler than it looks)
4. **Preview locally** - Download the [Stash viewer](https://thinkgo.io/stash) to see your changes rendered

## How to Contribute

### Quick Edits (Typos, Small Fixes)

1. Click the pencil icon on `regular_expressions.stash` in GitHub
2. Make your changes
3. Submit a pull request with a clear description

### Larger Contributions (New Sections, Examples)

1. Fork this repo
2. Clone your fork locally
3. Edit `regular_expressions.stash` in your preferred editor
4. Test with the Stash viewer (optional but recommended)
5. Commit with descriptive messages: `Add Unicode property escapes`
6. Push to your fork
7. Submit a pull request

## Stash Format Quick Reference

Lightweight and readable in raw form:
```stash
# Heading Level 1
## Heading Level 2

<cb>pattern_example<>

<c>inline_pattern<>

<b>bold text<>

<*>Bullet point
Another bullet<>
```

**Key elements:**
- `# Heading` - Section headers (use ## for subsections)
- `<cb>pattern<>` - Code/pattern blocks
- `<c>pattern<>` - Inline patterns
- `<*>item<>` - Bullet points
- `<#>comment<>` - Comments/notes

Full reference: https://speedsheet.io/s/stash

## Style Guidelines

**Pattern examples:**
- Keep them short and focused
- Show the pattern, then what it matches (and what it doesn't)
- Use realistic sample text when possible
- Note flavor-specific behavior where it differs

**Explanations:**
- Clear and concise - this is a reference, not a tutorial
- Lead with the most common use case
- Mention gotchas and edge cases
- Use active voice

**Organization:**
- Follow existing section structure
- Add `@` tags for search discoverability
- Cross-reference related patterns when helpful
- Note regex flavor if syntax is not universal

## Example Contribution

**Bad:**
```stash
### word boundary
matches word boundaries
```

**Good:**
```stash
### Word Boundary - \\b

<cb>\\bword\\b<>

Matches position between a word character (<c>\\w<>) and a non-word character. Zero-width (matches position, not characters).

<cb>"hello world" =~ /\\bworld\\b/   <#>// matches "world"<>
"helloworld" =~ /\\bworld\\b/    <#>// no match<><>

Use <c>\\B<> for the inverse (non-boundary positions).

@
@ word boundary, \\b, \\B, whole word
```

## Pull Request Guidelines

**Title format:**
- `Add [feature/topic]` - e.g., "Add possessive quantifiers"
- `Fix [issue]` - e.g., "Fix incorrect lookahead example"
- `Update [section]` - e.g., "Update Unicode categories for ES2024"

**Description should include:**
- What changed and why
- Regex flavor if specific (PCRE, JavaScript, Python, .NET, etc.)
- Link to documentation or spec if applicable

## Questions?

- **Format questions:** Check https://speedsheet.io/s/stash
- **Content questions:** Open an issue before large PRs
- **General questions:** Contact me using the [feedback form](https://speedsheet.io/feedback)

## License

By contributing, you agree that your contributions will be licensed under CC BY-NC-SA 4.0, matching the project license. You retain copyright but grant speedsheet.io and others the right to use your contribution under these terms.

---

**Bottom line:** Quality over quantity. A single well-crafted pattern example with clear match/non-match cases beats ten rushed additions. Take your time, and thank you for helping make this speedsheet better!
