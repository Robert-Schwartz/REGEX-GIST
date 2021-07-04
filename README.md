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

- Quantifiers Used: `+` , `{2,6}`
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

- Character Classes Used: `a-z`, `0-9`, `/d`, `/.`, `@`
    >* `a-z` looks for any characters within the range of lowercase a-z.
    >* `0-9` Looks for any characters within the range of 0 - 9.
     >* `/d` Matches any digit character (0-9). Equivalent to 0-9.
     >*  `/.`  Escape Character (period).  Escape sequences can be used to insert reserved, special, and unicode characters. All escaped characters begin with the `\` character.
      >* `@` Matches any @ character

<br> - Email Example: `validemail@gmail.com`

All characters contained in the email example are allowed by the Character Classes `a-z`, `0-9`, `/d`, `/.`, and `@` Therefore remaining valid

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


Groups allow you to combine a sequence of tokens to operate on them together. Capture groups can be referenced by a back-reference and accessed separately in the results.

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Groups used: `([a-z0-9_\.-]+)` , `([\da-z\.-]+)` , `([a-z\.]{2,6})`
    >* Group 1 is looking for any lowercase letter, any digit, any underscore, hyphen, period in a set prior to the `@` symbol.
    >* Group 2 is looking for any digit, lowercase letter, period, or hyphen prior to the escaped period `/.`
    >* Group 3 is searching for between 2-6 characters containing lowercase letters and/or a period.

<br> - Email Example: `validemail@gmail.com`
* Group 1 is `validemail`
* Group 2 is `gmail`
* Group 3 is `.com`


 ---

### Bracket Expressions:
<br>
A bracket Expression encloses a list of character classes within square brackets `[ ]`

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Bracket Expressions Used used: `[a-z0-9_\.-]` , `[\da-z\.-]` , `[a-z\.]`
    >* `[a-z0-9_\.-]` is searching for any lowercase letter, number, underscore, period, and/or hyphen.
    >*  `[/da-z.-] ` is searching for any digit, lowercase letter, period, and/or hyphen.
    >*  `[a-z\.] ` is searching for any lowercase letter, period and/or.

<br> - Email Example: `validemail@gmail.com`

All characters in `validemail@gmail.com` fulfill the bracket expressions constraints.

 ---
### Greedy and Lazy Match:
<br>
To specify the number of times a token should be matched by the regex engine you can use a greedy or lazy quantifier.
<br>

- Greedy Matching will attempt to match anything it can.
- Lazy matching will match as few characters as possible.
    * Lazy quantifiers are denoted by appending a ? to the quantifier symbol,

<br>

> Our Regex:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`

- Greedy Quantifier Used: `+` , `{2,6}`
    >* no lazy quantifiers were used

<br> - Email Example: `validemail@gmail.com`

 ---

 ---
 <br>

## Author:

Robert Schwartz
<br>
Github Profile:  Github.com/Robert-Schwartz
<br>
2021
