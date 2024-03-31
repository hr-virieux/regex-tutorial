# Validating Password Strength with Regex

This tutorial will explain how to use a regular expression (regex) to validate password strength for front end development. A strong password validation ensures that the user's chosen password meets specific security criteria, reducing the risk of unauthorized access.

## Summary

The following will explain a regex pattern designed to enforce passwords that include a mix of uppercase and lowercase letters, numbers, and special characters, and are of a certain length. The regex we'll analyze is as follows:

```regex
/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$/
```

This regex pattern is crucial for developers looking to implement robust password policies directly within their applications.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [The OR Operator](#the-or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

**`^` and `$`**

Anchors specify the start (`^`) and end (`$`) of the string, ensuring the entire password matches the pattern.

### Quantifiers

**`{8,}`**

Quantifiers indicate the number of characters. `{8,}` means the password must be at least eight characters long.

### The OR Operator

Not explicitly used in this regex pattern. The OR operator `|` is used to match one of several patterns.

### Character Classes

**`[A-Za-z\d@$!%*?&]`**

Character classes match any character within the brackets. This regex uses several classes to allow lowercase and uppercase letters, digits, and special characters.

### Grouping and Capturing

**`(?=...)`**

Grouping and capturing are used for look-ahead assertions, which ensure certain conditions are met without consuming characters.

### Bracket Expressions

Used within the character classes `[...]` to specify a set of characters to match.

### Back-references

Not used in this regex. Back-references allow a match to be referred again later in the regex.

### Look-ahead and Look-behind

**`(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])`**

Look-ahead assertions ensure the presence of lowercase letters, uppercase letters, digits, and special characters anywhere ahead in the string without including them in the match.

## Author

This tutorial was written by [Henry Virieux](https://github.com/hr-virieux).

Github Repo is located [here](https://github.com/hr-virieux/regex-tutorial).
