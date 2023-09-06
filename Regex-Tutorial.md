# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary 

A regex is a literal that must be wrapped using the `/` character. We will use the regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` to match emails as the example to help us understand regular expression.  This tutorial will give a detailed explanation of what a specific component of a regular expression.  In addition, it will also accomplish this using the the regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.

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

The characters `^` and `$` are considered as anchors. They act as start and end markers.

- `^` character signifies the start of a regular expression exclusive.
- `$` character signifies the end of a regular expression exclusive. 

#### For Example: 

The regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` would evaluate to `([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`.
The `/` at the beginning and end are the regular expression markers to denote that string is a regular expression.  The `^` denotes the start of the regular expression exclusive and the `$` denotes the end of the regular expression exclusive. 

### Quantifiers

Quantifiers limit the number of times and characters that can be matched.  
For example, `([a-z\.]{2,6}`, towards the end of our example regular expression, means our subexpression's matched pattern (`([a-z\.]`) length must be between 2 and 6 characters long.  This makes sense because the top level domain name generally appear towards the end of an email.

Quantifiers are inherently greedy, which we will describe in more detail in (#greedy-and-lazy-match) .

### OR Operator

The OR operator (`|`) allows for OR logic to be used in regular expressions.  It is especially helpful dealing with grouping contructs.

#### For Example: 
 A good example of using the OR operator would be to with we only wanted e,f, or g but limited to just efg.  This use of the OR operator would look something like: `(e|f|g)`.  Essentially, the OR operator gives us more flexibility. 


### Character Classes

A character class defines a set of characters.

Here are some of the most common character class:

- `.`  - Matches any character expect the newline character
- `/d` - Matches any numeric value, evaluates to `0-9`.
- `/w` - Matches any alphanumeric character including the underscore character, evaluates to `[A-Za-z0-9_]`.
- `/s` - Matches whitespace, which includes, the single whitespace character, tabs, and line breaks. 

#### For Example:
In our email example, we see `[\da-z\.-]+`, which includes `/d` representing `0-9`.

### Flags

Flags are placed after the closing slash to denote additional functionality or limits for the regex.

Some common flags include:
- `g` - Global search, the regular expression will be tested for multiple matches throughout the search string
- `i` - Case-insensitive search
- `m` - Multi-line search

### Grouping and Capturing

The main way of grouping a regular expression into subexpression is through the use of parentheses (`()`). Grouping constructs allow us to pattern match different sections to fulfill different requirements. 

#### For Example: 
In our email example, we have three different groups as followed: `([a-z0-9_\.-]+)` , `([\da-z\.-]+)`, and `([a-z\.]{2,6})`.

### Bracket Expressions

Anything inside the square brackets (`[]`) represents what the range of characters we want to match.  
Bracket expression are also known as positive character group because they describe the characters we want to include. The hyphen (`-`) character signifies we are dealing with a range of characters.

Capturing groups allow the matched characters to be re-used.  

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

#### For Example:
`[a-z0-9_\.-]+` means we must have at least one of this pattern in our email.  In simpler terms, we must have at least one lowercase, numeric, underscore, period, or hyphen character in our email.


### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

  If you have any questions, please here is my contact info:

  GitHub: fzhao888

  Email: frank.zhao93@gmail.com