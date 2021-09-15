# Gist Regex Tutorial

Regex or Regular expressions are patterns used to match character combinations in strings. In this tutorial we'll see how to use a regex to match email addresses.

## Summary

In this tutorial we'll be looking at how the following Regex is used to match an email address:

```js 
var emailRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
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

```js 
var emailRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
``` 

### Anchors ```^``` and ```$```

```^``` is used to find the start of the string.

```$``` is used to find the end of a string.

In our case it will start by looking for a group ```()``` and it will use the OR operator ```[]``` (explained below) to see what the criteria is.

### Quantifiers

### OR Operator

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
