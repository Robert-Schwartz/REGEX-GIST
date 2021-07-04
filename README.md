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



<br> - Email Example: `validemail@gmail.com`


Starts the check at the start of the email address and ends the check at the end of the string.

 ---


### Quantifiers:

  Quantifiers indicate that the preceding token must be matched a certain number of times.
  By default, quantifiers are greedy, and will match as many characters as possible.

> Our Regex:  `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

- Quantifiers Used: `+`  `{2,6}`
    >* `+` Matches 1 or more of the preceding token.
    >* `{2,6}` Matches the specified quantity of the previous token.

<br> - Email Example: `validemail@gmail.com`

1. `+` first follows the character set: `[a-z0-9_/.-]`.
2. This checks for 1 or more of those allowed characters: `(validEmail)`.
3. `{2,6}` follows the character set: `[a-z\.]`.
4. This quantifier says "Match between 2 and 6 of the preceding characters: `(.com)`.


 ---

### Character Classes:


Character Classes match a character from a specific set.  There are pre-defined classes or you can define unique sets.  Character classes can also be combined in a large set.

> Our Regex:  `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

- Anchors Used: `[a-z]`, `[0-9]`, `/d`, `/.`
    >* `[a-z]` looks for any characters within the range of lowercase a-z.
    >* `[0-9]` Looks for any characters within the range of 0 - 9.
     >* `/d` Matches any digit character (0-9). Equivalent to [0-9].
     >*  `/.`  Escape Character (period).  Escape sequences can be used to insert reserved, special, and unicode characters. All escaped characters begin with the `\` character.

<br> - Email Example: `validemail@gmail.com`

This email contains characters allowed by the Character Classes `[a-z]`, `[0-9]`, `/d` and `/.`, Therefore remains valid

 ---


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
