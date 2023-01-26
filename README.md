# Regex-Tutorial

This Regular Expression (Regex) tutorial is created as a walk through of the functions of Regular Expressions, This is great for pulling out information from a given body of code and also can serve as well as a tool for validation. A Regex is a series of characters which defines a specific type of search pattern when included in a code or search algorithm, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also used frequently to validate input data.

## Summary

The following code will be used throughout the tutorial to give specific examples for how the components of regex can be used. The following code can be used for matching emails. One use for this code is that it can be used to validate to make sure that an email follows the correct format.

Matching an Email - /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are what starts and ends the regular expression. In this email code,

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/,

the anchors are the ^ and the $. This code is telling the computer that we are looking for strings that starts with

^([a-z0-9_.-]+)

and end with

.([a-z.]{2,6})$.

therefore, it must begin and end with the given parameters within the code. otherwise, it is not a match.

### Quantifiers

A quantifier is used to determine how many times a specific character or sequence of characters needs to be present in order to match. take the following code for matching the email:

([a-z0-9_.-]+)

It will match any string that contains a-z, 0-9, _, ., or -. The quantifier + means it must contain at least one of these to be a match.

### Grouping Constructs

Grouping constructs are used to group together a set of characters, quantifiers, or other regular expressions. They are represented by parentheses `()`.

Grouping constructs are used to group specific parts of the email address. The regular expression has three groups:

`([a-z0-9_.-]+)`: matches one or more characters that are lowercase letters, digits, underscores, periods, or hyphens and represents the username of the email address.
`([\da-z.-]+)`: matches one or more characters that are digits, lowercase letters, periods, or hyphens and represents the domain name of the email address.
`([a-z.]{2,6})`: matches two to six characters that are lowercase letters or periods and represents the top-level domain (TLD) of the email address.
These groups allow you to refer to specific parts of the match later, for example you could use the group to extract the username, domain name, and TLD from the email address.

It also allows you to apply quantifiers or other operators to the entire group of characters rather than just one character. For example, in the first group `([a-z0-9_.-]+)` the `+` quantifier is applied to the entire group of characters, which means to match one or more of the characters within the group.

### Bracket Expressions

A bracket expression is anything inside of square brackets `([])` represents the range of characters we want to match.

username: ([a-zA-Z0-9._-]+)
email host name: ([a-zA-Z0-9._-]+)
domain: ([a-zA-Z]{2,4})

### Character Classes

Character classes are used to match a set of characters. They are represented by square brackets `[]` and can contain individual characters, ranges of characters, or a combination of both.

In the expression provided above are several character classes:

[a-z]: matches any lowercase letter
[0-9]: matches any digit
[._-]: matches any of the characters _, ., or -
[\da-z.-]: matches any digit, lowercase letter, period or hyphen
[a-z.]: matches any lowercase letter or period

These character classes are used to ensure that the email address is in the correct format and that only valid characters are used in the specific parts of the email address.
The character class [a-z0-9_.-] is within a group `()` and is followed by the `+` quantifier which means to match one or more of the characters within the class.

### The OR Operator

The expression I provided above does not use The Or Operator. But The `OR` operator within a regular expression is defined using the `|` element. The component indicates that it could be either of the components that we are separating with the `|`. 

### Flags

This expression I am using above does not have any flags. In regular expressions though, flags are used to modify the behavior of the regular expression. They are added after the last delimiter `/` and can be combined. Some common flags include:

`i`(case-insensitive): matches the pattern regardless of the letter case
`g` (global search): matches all occurrences of the pattern in the input text, not just the first
`m` (multiline): allows the use of ^ and $ to match the beginning and end of each line, rather than the entire input string.

### Character Escapes

This regular expression is used to validate email addresses. It checks that the email address starts with one or more characters that are lowercase letters, digits, underscores, periods, or hyphens (^([a-z0-9_.-]+)), followed by an at symbol (@), followed by one or more characters that are digits, lowercase letters, periods, or hyphens   (`([\da-z.-]+)`), followed by a period (`.`), and finally two to six characters that are lowercase letters or periods (`([a-z.]{2,6})$`). The slashes `/` are used to delimit the regular expression.

The backslash `\` is used as an escape character in regular expressions. It is used before certain characters (such as `.` or `$`) to indicate that they should be treated as literal characters rather than special characters with a special meaning in regular expressions. In this regular expression, the backslash is used before the `d` and `.` to treat them as literal characters.

## Author

Written by [Janvier Barreto](https://github.com/JanvierB1/Regex-Tutorial.git)
