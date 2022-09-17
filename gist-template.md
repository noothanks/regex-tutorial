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

### Anchors

Anchors are a type of regex token that do not match with any characters. Instead, they do things like indicate the beginning and end of a line or string.

Examples for our expression include:
 * ^ indicates the beginning of a string or a line
 * $ indicates the end of a string or a line


### Quantifiers

Quantifiers give important information on how many characters of a certain type should be grouped together.
Examples:
    * + matches a string that has at least one of its associated characters
    * * indicates zero or more of its associated character
    * ? matches a string that has zero or one of its associated characters
    * {4} matches a sequence of four associated characters
    * {2,5} matches a sequence between two and five associated characters (inclusive)

### OR Operator

The OR operator accepts any amount of specifications as long as they are separated by a "|" character

Example:
    * dogs|cats will expect either dogs or cats

### Character Classes

Character classes designate a group of characters to a single special character
    Examples:
        * \w matches any word character (letter or number 0-9)
        * \d matches any number 0-9


### Flags

Flags are responsible for changing the default searchfunctionality
    * i performs a case-insensitive search
    * g performs a global search and finds all cases 

### Grouping and Capturing

Grouping is indicated by () characters around a section of a regex. This allows the expression to be broken down into smaller chunks.
* (asd) will match asd
* (asd) will not match with dsa, as (asd) looks for an identical match 

### Bracket Expressions

Bracket expressions are performed by using [] to define a group of characters you would like to search for
Examples:
    * [a-z] will search for the lowercase alphabet
    * [A-Z] will search for the uppercase alphabet
    * [^a-z] will search for any characters that are not of the lowercase alphabet

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
