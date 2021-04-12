# RegexEmailVerify

This tutorial will detail using an email verification regex express for someone desiring to undertand how and the why using regex expression works. 

## Summary

This tutorial will detail the workings of an email verification regex expression. This tutorial will include how the different search boundaries are utillized and include an example of each of those boundaries. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+).([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Author](#author)

## Regex Components

### Anchors

```
Anchors are the opening and closing strings of a regex expression. The opening anchor includes a caret, ` ^ `. The closing anchor includes the dollar symbol, ` $ `.

/^([a-z0-9_\.-]+)@([\da-z\.-]+).([a-z\.]{2,6})$/

For the regex email verification , the opening anchor is `/^` and the closing anchor is `$\`. 
```

### Quantifiers
```
Quantifiers are expressions that come directly to the left of a particular quantity of the character, token or subexpression. 

* quantifier allows for the engine to match 0 or more characters
+ quantifier allows for the engine to match 1 or more characters
{#,#} quantifier sets a {min,#} and a {#,max} for the character values
{#} quantifier can be set to a single numerical value. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+).([a-z\.]{2,6})$/

In the regex email verification, the `{2,6}` sets the minimum charcters allowed after the `.com` to be 2 and the maximum characters  allowed to be 6. 

Another example is the `+` which is added after the first set of `[]` which is the first word of the email address and the second set of `[]` which is the  second word of the email address. This shows that the search engine searches for one or more characters. 
```

### Character Classes
```
Character Classes inform the search engine what characters are allowed in the expression. These classes are included within `[]`. 

An example of this is the different way to spell something. There are two ways to spell adapter or adaptor. To write a class to allow the search engine to search for either- the express would denote this as such adapt[eo]r.

/^([a-z0-9_\.-]+)@([\da-z\.-]+).([a-z\.]{2,6})$/

In the regex email verification, there are 3 character classes. 
The first one is [a-z0-9_\.-]
The character class will search for:
letters a-z (lowercase or uppercase) `a-z`,
numbers 0-9 `0-9`,
an underscore `_`, 
a period `\.`,
and a dash `-`. 

The second class is [\da-z\.-]
The character class will search for:
any number 0-9, `\d`,
letters a-z (lowercase or uppercase) `a-z`,
a period `\.`,
and a dash `-`.

The third class is [a-z\.]
The character class will search for:
any letter a-z (lowercase or uppercase) `a-z`,
and a period `\.`.

```
### Grouping and Capturing
```
Grouping allows for a search of characters within their own particular group. 
Capturing allows for a serach of all the characters in a particular group. 

An example of how a user could search using grouping to order a list of names. Here is a list of names:

Olivia Pope
Fitzgerald Grant
Mellie Grant
Cyrus Bean
Quinn Perkins

To gather the first and last names in two different groups, using the notation `(\w+)\s+(\w+)` with sort these. 

The first `(\w+)` will take the first name and assign it to Group 1. 
The `\s+` matches a single white space character for Group 1 with Group 2. 
The second `(\w+)` will take the second name and assign it to Group 2. 

To reorder the list by alphabetical order, the expression woulld be `$1 $2`.

`$1` is referring to Group 1 which captures all the first names. 
`$2` is referring to Group 2 which captures all the last names. 
` ` is referring to the space between both names. 

Running the code will now have the list displayed as this:
Cyrus Bean
Fitzgerald Grant
Mellie Grant
Olivia Pope
Quinn Perkins


/^([a-z0-9_\.-]+)@([\da-z\.-]+).([a-z\.]{2,6})$/

In the regex email verification, `()` are capturing each group. 

Group 1: 
This will capture the username.
([a-z0-9_\.-]+)

Group 2: 
This will capture the domain name
([\da-z\.-]+)

Group 3: 
This will caputre the extension
([a-z\.]{2,6})
```
## Author

```

Brittany's contacts:

Email: (BLee@BrittanyLeeConsulting.com)

Github: (https://github.com/blee2013)

LinkedIn: (https://www.linkedin.com/in//brittany-lee-6142121b8/)

```