# Email Matching Using REGEX

This Gist will describe the process of using a regular expression in order to match the characters of a text string to verify that it is a valid email address format.


## Summary

The following regular expression can be used to verify that user input is a valid email address:

>`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The Contents below will break down this expression into it's parts.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors:


Anchors match a position within a string

> Our Regex:  `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

- Anchors Used: `^` , `$`
    >* `^` Indicates the Starting Position
    >* `$` Indicates the Ending Position



- Email Example: `validemail@gmail.com`


Starts the check at the start of the email address and ends the check at the end of the string.

 ---


### Quantifiers:

  Quantifiers indicate that the preceding token must be matched a certain number of times.
  By default, quantifiers are greedy, and will match as many characters as possible.

> Our Regex:  `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

- Quantifiers Used: `+`  `{2,6}`
    >* `+` Matches 1 or more of the preceding token.
    >* `{2,6}` Matches the specified quantity of the previous token.

- Email Example: `validemail@gmail.com`

1. `+` first follows the character set: `[a-z0-9_/.-]`.
2. This checks for 1 or more of those allowed characters: `(validEmail)`.
3. `{2,6}` follows the character set: `[a-z\.]`.
4. This quantifier says "Match between 2 and 6 of the preceding charachters: `(.com)`.


 ---

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Robert Schwartz
Github Profile:  Github.com/Robert-Schwartz
