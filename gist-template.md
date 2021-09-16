# Gist Regex Tutorial

Regex or Regular expressions are patterns used to match character combinations in strings. In this tutorial we'll see how to use a regex to match email addresses.

## Summary

In this tutorial we'll be looking at how the following Regex is used to match an email address:

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;
```

We'll walk-through each of the components to determine how they work and why we're using them.

## Table of Contents

- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;
``` 

### Quantifiers ```+ {}```

```+``` Matches a string that has the specified characters on the left side followed by one or more items on the right side.

e.g. in our section of code:

```([\w\.]+) => [\w\.]``` Matches any word character equivalent to ```\w = [a-zA-Z0-9_]``` or ```\.``` matches the character "." one or more times.
____

```{}``` Sets either an exact amount, min and max, or more than one copies of the sequence before the quantifiers.

e.g. in our section of code:

```([a-z\.]{1,3})``` matches the previous token (```[a-z\.]```) between 1 and 3 times, as many times as possible.

### OR Operator ```[] [^...]```
```[]``` Matches a character that is contained within the brackets.

e.g. in our section of code:

```[a-z]``` Matches the range of lower case letters from "a" to "z".

___

```[^...]``` Matches a character that _is not_ contained within the brakets. 

e.g. in our section of code:

```[^\W_]``` Matches any character that is not present in the list. 
```\W``` Matches any non-word character (```[^a-zA-Z0-9_]```) and ```_``` matches the character "_".

### Character Classes ```\d \w```

```\d``` Matches a single character that is a digit.

```\w``` Matches a word character, i.e. [a-zA-Z0-9_].

### Flags ```g```

When writing Regex the search parameters are delimeted by two slash characters ```/.../``` . At the end i.e. after the second slash character is where we specify theflags.

```g``` (global) It allows for the search to continue after the first match and to continue until no more matches can be found.

### Grouping and Capturing ```()```

```()``` Captures everything enclosed within the parenthesis. It isolates part of the full match and assignes it an ID to be later referred to within the regex.

### Boundaries ```\b```

Matches on a word boundary, meaning one side is a word character (like ```\w```) and the other side is not a word character (like a space character).

## Author

[kmre - A newbie programmer](https://github.com/kmre)
