# Email Matching Using REGEX

This Gist will describe the process of using a regular expression in order to match the characters of a text string to verify that it is a valid email address format.


## Summary

The following regular expression can be used to verify that user input is a valid email address:

>`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

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
---

## Regex Components

<br>

### Anchors:
<br>


Anchors match a position within a string

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Anchors Used: `^` , `$`
    >* `^` Indicates the Starting Position
    >* `$` Indicates the Ending Position



<br> - Email Example: `validemail@gmail.com`


Starts the check at the start of the email address and ends the check at the end of the string.

 ---


### Quantifiers:
<br>

  Quantifiers indicate that the preceding token must be matched a certain number of times.
  By default, quantifiers are greedy, and will match as many characters as possible.

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

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
<br>


Character Classes match a character from a specific set.  There are pre-defined classes or you can define unique sets.  Character classes can also be combined in a large set.

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Character Classes Used: `[a-z]`, `[0-9]`, `/d`, `/.`, `@`
    >* `[a-z]` looks for any characters within the range of lowercase a-z.
    >* `[0-9]` Looks for any characters within the range of 0 - 9.
     >* `/d` Matches any digit character (0-9). Equivalent to [0-9].
     >*  `/.`  Escape Character (period).  Escape sequences can be used to insert reserved, special, and unicode characters. All escaped characters begin with the `\` character.
      >* `@` Matches any @ character

<br> - Email Example: `validemail@gmail.com`

All characters contained in the email example are allowed by the Character Classes `[a-z]`, `[0-9]`, `/d`, `/.`, and `@` Therefore remaining valid

 ---


### Flags:
<br>


Regular expressions have six optional flags that allow for functionality like global and case insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Flags used: `g`
    >* `g` is used as a Global search and will match all occurrences.<br>Without the `g` flag, it'll only test for the first.

<br> - Email Example: `validemail@gmail.com`

There was one global occurrence of this email address.

 ---


### Grouping and Capturing:
<br>


Regular expressions have six optional flags that allow for functionality like global and case insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Flags used: `g`
    >* `g` is used as a Global search and will match all occurrences.<br>Without the `g` flag, it'll only test for the first.

<br> - Email Example: `validemail@gmail.com`

There was one global occurrence of this email address.

 ---

### Bracket Expressions:
<br>

 ---
### Greedy and Lazy Match:
<br>

 ---
### Boundaries:
<br>

 ---
### Back-references:
<br>

 ---
### Look-ahead and Look-behind:
<br>

 ---
## Author:

Robert Schwartz
<br>
Github Profile:  Github.com/Robert-Schwartz
<br>
2021
