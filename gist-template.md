# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

A regex is a literal that must be wrapped using the `/` character. We will use the regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` to match emails as the example to help us understand regular expression. Its components are described as follows.

### Anchors

The characters `^` and `$` are considered as anchors. They act as start and end markers.

- `^` character signifies the start of a regular expression exclusive.
- `$` character signifies the end of a regular expression exclusive. 

#### For Example: 

The regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` would evaluate to `([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`.
The `/` at the beginning and end are the regular expression markers to denote that string is a regular expression.  The `^` denotes the start of the regular expression exclusive and the `$` denotes the end of the regular expression exclusive. 

### Quantifiers

Quantifiers limit the number of times and characters that can be matched.  
For example, `{2,6}`, towards the end of our example regular expression, means our matched pattern's length must be between 2 and 6 characters long.  
They are inherently greedy, which we will describe in more detail in (#greedy-and-lazy-match) .

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

The main way of grouping a regular expression into subexpression is through the use of parentheses (`()`). 

#

### Bracket Expressions

Anything inside the square brackets (`[]`) represents what the range of characters we want to match.  
Bracket expression are also known as positive character group because they describe the characters we want to include. The hyphen (`-`) character signifies we are dealing with a range of characters.

#### For Example:

The possible pool of characters for `[a-z0-9_\.-]` would evalute to all lowercase, numeric, underscore, period, and hyphen characters.


### Greedy and Lazy Match

As we stated earlier, quantifiers are inherently greedy.  A greedy match is a match that can match many occurrences of a particular patterns as possible.  They include the following:

- `*` - Matches the pattern zero or more times
- `+` - Matches the pattern one or more times
- `?` - Matches the pattern zero or one times

- `{}` - There are three different limits:
    - 1) `{n}` - Matches the pattern exactly n times
    - 2) `{n}` - Matches the pattern at least n times
    - 3) `{n,x}` - Matches the pattern a minimum of n times and a maximum of x times. 

#### For example,
`[a-z0-9_\.-]+` means we must have at least one of this pattern in our email.  In simpler terms, we must have at least one lowercase, numeric, underscore, period, or hyphen character in our email.


### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
