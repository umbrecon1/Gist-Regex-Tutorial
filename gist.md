# Testing A Strong Password

Regular expressions are a sequence of characters that forms a search pattern, mainly for use in pattern matching with stings, or string matching. For this assignment, I will be breaking down how to utilize that to test a strong password.

## Summary

```
^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[!@#\$%\^&\*])(?=.{8,})
```
- **^** The password string will start this way.

- **(?=.*[a-z])** The string must contain at least 1 lowercase alphabetical character

- **(?=.*[A-Z])** The string must contain at least 1 uppercase alphabetical character

- **(?=.*[0-9])** The string must contain at least 1 numeric character

- (?=.*[!@#$%^&*]) The string must contain at least one special character, but we are escaping reserved RegEx characters to avoid conflict

- **(?=.{8,})** The string must be eight characters or longer



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

- **^** This is our sting anchor. It matches the start of the string the regex pattern is applied to.

### Quantifiers

- Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. Here we have '*' to show each type of character needs to be used at least once. In the case of **{8,}**, it shows we need at least 8 characters.

### Grouping Constructs

- We have a total of 5 grouping constructs all seperated by "()"

- **(?=.*[a-z])**
- **(?=.*[A-Z])**
- **(?=.*[0-9])**
- (?=.*[!@#$%^&*])
- **(?=.{8,})**

### Bracket Expressions

- Use bracket expressions to match single characters in a list, or a range of characters in a list. If the first character of the list is the carat ^ then it matches characters that are not in the list.

- **[a-z]** Matches lowercase letters from a-z
- **[A-Z]** Matches uppercase letters from A-Z
- **[0-9]** Matches numbers 0-9
- **[!@#$%^&*]** Matches special characters listed

### Character Classes

- A character class. Matches any one of the enclosed characters. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character.
**See above for the same usage**

### The OR Operator

- You can use the | operator to match characters or expression of either the left or right of the | operator.
**We do not use | for this specific regex.**


## Author

- My name's Connor Mitchener.I'm a student in the UCI Bootcamp and an aspiring web developer.

- Link: www.github.com/umbrecon1

