# Breaking Down Regex: Matching an Email Example

Regex expressions are used as a predictive measure of a string. This can be used to expect a certain pattern of characters when searching for a string.

## Summary

Our example will use a simple email regex expression that expects the pattern of a typical email address. This breakdown will explain the different pieces of a regex expression and show how they are present in our example.

We will be using the following expression:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are a type of regex token that do not match with any characters. Instead, they do things like indicate the beginning and end of a line or string.

Examples:
 * ^ indicates the beginning of a string or a line
 * $ indicates the end of a string or a line

Here we see both characters listed above in our expression:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The /^ lets us know that its the beginning of our email string, while the $/ indicates that its the end of our email string.


### Quantifiers

Quantifiers give important information on how many characters of a certain type should be grouped together.
Examples:
    * + matches a string that has at least one of its associated characters
    * * indicates zero or more of its associated character
    * ? matches a string that has zero or one of its associated characters
    * {4} matches a sequence of four associated characters
    * {2,5} matches a sequence between two and five associated characters (inclusive)

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Our expression uses the + character to say that we're expecting one or more groups of [a-z)0-9\.-] and one or more groups of [\da-z\.-].

We can also see the use of a sequence quantifier in {2,6} above. This says to expect at least two, but no more than six groups of [a-z\.].



### OR Operator

The OR operator accepts any amount of specifications as long as they are separated by a "|" character.

Example:
    * dogs|cats will expect either dogs or cats

### Character Classes

Character classes designate a group of characters to a single special character.
    Examples:
        * \w matches any word character (letter or number 0-9)
        * \d matches any number 0-9

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Our email regex uses the \d character class to indicate we're expecting any digit from 0-9. This is seen above in the grouping [\da-z\.-].

### Flags

Flags are responsible for changing the default searchfunctionality
    * i performs a case-insensitive search
    * g performs a global search and finds all cases 

### Grouping and Capturing

Grouping is indicated by () characters around a section of a regex. This allows the expression to be broken down into smaller chunks. Substrings grouped by () will be captured separately as a backreference.
* (asd) will match asd
* (asd) will not match with dsa, as (asd) looks for an identical match 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We have several groups of substrings above indicated by their surrounding parentheses.

### Bracket Expressions

Bracket expressions are performed by using [] to define a group of characters you would like to search for
Examples:
    * [a-z] will search for the lowercase alphabet
    * [A-Z] will search for the uppercase alphabet
    * [^a-z] will search for any characters that are not of the lowercase alphabet

### Greedy and Lazy Match
Greedy matches will try to match as much as possible, while lazy matches will.
Examples: 
    * <.+> is a greedy search that will match with an opening < up to and including the closing >
    * <.+?> is a lazy search that will only match with the first instance of a < character

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Matches are greedy by default, and can be used in combination with grouping. For an example used in our expression, see the quantifiers section.

### Boundaries

Boundaries allow for a more specific search by specifying the beginning and end of the word you are looking for.

Examples:
    * \bhotdog\b will look for the entire word hotdog
    * \Bhotdog\B will match where hotdog is not 


## Author
There's a lot of code out there and a lot more to learn.
Check out my github page and learn with me:
 * [@noothanks](https://www.github.com/noothanks)
