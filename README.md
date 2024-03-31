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
- [Character Classes](#character-classes)
- [Lookahead Assertions](#lookahead-assertions)
- [Examples](#examples)
- [Author](#author)

## Regex Components

### Anchors

**`^` and `$`**

Anchors denote the start (`^`) and the end (`$`) of the string, ensuring the entire password matches the specified pattern. They are crucial in validating that the password does not contain any characters or sequences outside the defined criteria.

### Quantifiers

**`{8,}`**

The `{8,}` quantifier indicates that the password must be at least eight characters in length. It is applied to the combined character set `[A-Za-z\d@$!%*?&]`, reinforcing the minimum length requirement for the password.

### Character Classes

**`[A-Za-z\d@$!%*?&]`**

Character classes match any single character within the brackets. In our regex, several classes are used to permit lowercase and uppercase letters, digits, and specified special characters, offering flexibility in password composition.

### Lookahead Assertions

**`(?=.*[a-z])`, `(?=.*[A-Z])`, `(?=.*\d)`, `(?=.*[@$!%*?&])`**

Lookahead assertions are utilised to check for the presence of certain character types within the password without consuming characters. They ensure the password contains at least one lowercase letter, one uppercase letter, a digit, and a special character from the set `[@$!%*?&]`.

## Examples

To demonstrate the application of our regex, consider the following examples:

- **Valid Passwords:**
  - `Password1!` meets all criteria: it has uppercase and lowercase letters, a digit, and a special character.
  - `Another$ecure2` also satisfies the requirements, showcasing the flexibility in character positions.

- **Invalid Passwords:**
  - `pass` is too short and lacks uppercase letters, digits, and special characters.
  - `password` meets the length requirement but fails to include uppercase letters, digits, and special characters.

These examples elucidate how the regex filters passwords based on the defined strength criteria.

## Author

This tutorial was written by [Henry Virieux](https://github.com/hr-virieux).

Github Repo is located [here](https://github.com/hr-virieux/regex-tutorial).
