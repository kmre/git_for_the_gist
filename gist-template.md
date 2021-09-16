# Gist Regex Tutorial

Regex or Regular expressions are patterns used to match character combinations in strings. In this tutorial we'll see how to use a regex to match email addresses.

## Summary

In this tutorial we'll be looking at how the following Regex is used to match an email address:

<!-- ```js 
var emailRegex = /^([a-z0-9_\.]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
```  -->

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/gm;
```

We'll walk-through each of the components to determine how they work and why we're using them.

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

<!-- ```js 
var emailRegex = /^([a-z0-9_\.]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
```  -->

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/gm;
``` 

### Anchors ```\b```

Matches on a word boundary, meaning one side is a word character (like ```\w```) and the other side is not a word character (like a space character).

<!-- ### Anchors ```^``` and ```$``` -->

<!-- ```^``` is used to find the start of the string.

```$``` is used to find the end of a string.

In our case it will start by looking for a group ```()``` and it will use the OR operator ```[]``` (explained below) to see what the criteria is. -->

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


### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
