# Title (replace with your title)

This project is a walk through of what a regular expression is and how to use it and understand it. Regular expressions, or Regex, can be used when the user wants to match character combinations within a string. This method is used to extract information from any given body of code and used for validation. This tutorial will show an example of a code snippet that can be used to match an email.

## Summary

The following code will be used throughout the tutorial to give specific examples for how the components of regex can be used.

Matching Email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

The anchor is what starts and ends the regular expression. In the matching email code,

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/,

the anchors are the ^ and the $. This code specifically is saying that we are looking for something that starts with

^([a-z0-9_\.-]+)

we will define what everything inside the parentheses later in this tutorial, but what the anchor means is that if we are to find a match it has follow those initial guidelines. It also has to end with

.([a-z\.]{2,6})$.

So, it must start and end with the given parameters within the code. If it does not, then it is not a match.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
