# C-17-CS-for-JS_Regex-Tutorial

This is a tutorial on Regular Expressions (regex) in JavaScript.
Regular Expressions are a pattern matching language that can be used to match a string against a subject string from left to right.

## Summary

In this tutorial, I'm going to explain the Regular Expression (regex) for the validation of an email address.

Matching an Email – `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to check if the matching symbol is the start or end of the string. Two types of anchors are supported: `^` (caret) and `$` (dollar sign).

`/^[a-z]/` check if a matching character is the first character of the input string
`/[a-z]$/` check if a matching character is the last character in the string

### Quantifiers

Quantifiers are used to specify the number of times that a character or a group of characters are expected to occur in the input string. Two types of quantifiers are supported: `+` (plus sign) and `{}` (curly braces).

The `+` symbol matches one or more repetitions of the preceding character.

`[a-z0-9_\.-]+` any character is expected to occur at least once

The `{}` are used to specify the number of times that a character or a group of characters can be repeated.

`[a-z\.]{2,6}` match at least 2 times but not most 6 times

### Character Classes

Character Classes are used to specify a set of characters that are expected to occur in the input string.

`[ABC]` match any of the characters in the brackets

`[a-z] and [0-9]` match a character between a and z or a digit between 0 and 9

`.` match any single character except a line break

`\d` match any digit between 0 and 9. Equivalent to `[0-9]`

### Grouping and Capturing

A capturing group is a group of sub-patterns that is inside `()` (parentheses).

Group #1: `([a-z0-9_\.-]+)` matches the username

Group #2: `([\da-z\.-]+)` matches the domain/email service

Group #3: `([a-z\.]{2,6})` matches the top level domain

### Bracket Expressions

Bracket expressions are a list of characters and/or character classes enclosed in brackets [], used to match single characters in a list, or a range of characters in a list.

`[a-z0-9_\.-]` matches any character from a to z, 0 to 9, underscore, dot, or dash

`[\da-z\.-]` matches any digit from 0 to 9, a to z, dot, or dash

`[a-z\.]` matches any character from a to z, or dot

### Greedy and Lazy Match

A `Greedy` quantifier always attempts to repeat the sub-pattern as many times as possible before exploring shorter matches by backtracking. By default, all quantifiers are greedy.

`+` will match as many times as possible.

`{}` will match exactly n times.

## Author

Diego Kaku is a Web Developer Student at the University of Minnesota Coding Bootcamp.

GitHub profile: https://github.com/kakudiego
