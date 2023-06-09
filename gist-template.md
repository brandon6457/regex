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

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, xyz+ then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

([a-z0-9_\.-]+)

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier + means that it has to contain at least one of this in order to have a match.

### Grouping Constructs

Continuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

([a-z0-9_\.-]+) is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. ([\da-z\.-]+) is the second group that appears in our regex. ([a-z\.]{2,6}) is the third group that appears in our regex.

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group.

### Bracket Expressions

Continuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The following is the bracket expression.

[a-z0-9_\.-]

The guidelines for matching the group. For this code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period.

The period is an escaped character, so it required the backslash in order to be able to be matched.

### Character Classes

\d is present in the given matching email code and what it will match a single letter character, a-z, after the @ sign in the email address. Basically ensuring that a letter is matched after the @ in the email and not a number or special character.

### The OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

This is a regex for matching a hex code that uses the OR Operator. What this will do is it will match where it starts with the # and that has to come first followed by one of the following:

[a-f0-9]{6} which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers.

| OR Operator

[a-f0-9]{3} it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers.

### Flags

A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

/regex/

Where the slashes denote where the regular expression starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:

g which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
m which stands for "multiline" which will search line by line rather than searching through a string as a whole.
i which stands for "insensitive" will make the regular expression case-insensitive, so capitals and lower-case letters will not deter the matching.

### Character Escapes

Based on the regex email code /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ the character escapes are as follows:

\d: Matches any digit (equivalent to [0-9])

\.: Matches a period/dot character

\-: Matches a hyphen-minus character (needs to be escaped within square brackets to avoid being interpreted as a range)

[a-z0-9_\.-]: Matches any lowercase letter, digit, underscore, period or hyphen-minus character

[a-z\.]: Matches any lowercase letter or period character (used in the TLD of the email domain)

Note that the backslashes () are used to escape the special meaning of certain characters and treat them as literal characters in the regex pattern.

## Author

This tutorial was written by [Brandon Morgan](https://github.com/brandon6457). By clicking on my name, you can view other repositories that I have created and contributed to.
