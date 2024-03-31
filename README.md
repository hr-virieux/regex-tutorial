# Validating Hex Values with Regex

This tutorial will explain the use of a regular expression (regex) to validate hexadecimal values. Hexadecimal values, often used to define colours in web development, consist of numbers and the letters A-F. Validating such values is crucial for ensuring input data adheres to expected formats in web applications.

## Summary

Our focus will be on explaining a regex pattern designed for validating hex values:

```regex
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

This pattern is essential for developers looking to verify colour codes or other hex-based data inputs.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Conditional OR](#conditional-or)
- [Examples](#examples)
- [Author](#author)

## Regex Components

### Anchors

**`^` and `$`**

Anchors are used to denote the beginning (`^`) and the end (`$`) of the string, ensuring the entire hex value matches the specified pattern without any leading or trailing characters.

### Quantifiers

**`{6}` and `{3}`**

Quantifiers specify the number of characters. `{6}` means the hex value must have exactly six characters, and `{3}` indicates a shorter format with three characters. These quantifiers accommodate both full and shorthand hex colour codes.

### Character Classes

**`[a-f0-9]`**

Character classes allow for the matching of any single character within the brackets. In our regex, `[a-f0-9]` matches any hexadecimal character, which includes digits (`0-9`) and lowercase letters (`a-f`). This ensures that the input is within the hexadecimal range.

### Conditional OR

**`|`**

The conditional OR (`|`) allows for the matching of one of several subpatterns. In this case, it distinguishes between full (`{6}` characters) and shorthand (`{3}` characters) hex formats, providing flexibility in what is considered a valid hex value.

## Examples

To demonstrate the application of our regex, consider the following examples:

- **Valid Hex Values:**
  - `#ffffff` matches the full hex format.
  - `#abc` matches the shorthand hex format.
  
- **Invalid Hex Values:**
  - `#gggggg` is invalid as `g` is outside the hexadecimal range.
  - `123456` is invalid as it lacks the leading `#`.

These examples illustrate how the regex filters hex values based on the defined criteria, ensuring only valid hex codes are accepted.

## Author

This tutorial was written by [Henry Virieux](https://github.com/hr-virieux).

Github Repo is located [here](https://github.com/hr-virieux/regex-tutorial).
