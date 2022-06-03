# Computer Science for JavaScript: Regex Tutorial

Regular expressions can be used to find certain patterns of characters within a string. You can also find and replace a character or sequence of characters within a string. They are also frequently used to validate input. This regex matches character information for valid e-mail addresses. Also, a regular expression is a pattern that the regular expression engine attempts to match in input text. A pattern consists of one or more character literals, operators, or constructs

## Summary

The following code will be used throughout the tutorial to give specific examples for how the components of regex can be used. The following code can be used for matching emails. One use for this code is that it can be used to validate to make sure that an email follows the correct format.

Matching Email-

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
The anchors used to contain this regular expression are: "^" to start, and "$" to finish.

### Quantifiers
for this this example, we used "+" to communicate there is another sequence to be matched as a greedy quantifier. We also used "{2,6}" as another greedy quantifer to specify the input should be a minimum of 2 characrtors to a maximum of 6 characters.

### Grouping Constructs
There are three groups being captured in this example. Group #1 is the username of the e-mail account "[a-z0-9_\.-]". The second group captures the domain name or e-mail service being used "[\da-z\.-]". Lastly, the third group captures the domain extention (i.e .com or .net) "[a-z\.]{2,6}"

### Bracket Expressions
Anything inside a set of square brackets "([])" represents a range of characters that we want to match. These patterns are known as bracket expressions.

Contininuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping and capturing.

" [a-z0-9_\.-]"

The guidelines for matching the group. For this code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period.

The period is an escaped character, so it required the backslash in order to be able to be matched.

### Character Classes
\d is present in the given matching email code and what it will match a single letter character, a-z, after the @ sign in the email address. Basically ensuring that a letter is matched after the @ in the email and not a number or special character

### The OR Operator
the Or operator is not on our givin regex code. So instead we will be using this for this part: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The "or" operator within a regular expression is defined using the | element. The or operator indicates that it could either of the components that we are separating with the |. For our hex value regular expression we have " ([a-f0-9]{6}``|``[a-f0-9]{3})" . Note the or operator separating these 2 components. This means that our hex value could either be 6 characters [a-f0-9]{6} or 3 characters [a-f0-9]{3}.


### Flags
 Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex.

 The following are the most common that you will encounter:

- g — "Global search" : the regex should be tested against all possible matches in a string.

- i — "Case-insensitive search": case should be ignored while attempting a match in a string

- m — "Multi-line search": a multi-line input string should be treated as multiple lines

### Character Escapes

"\d" is present in the given matching email code and what it will match a single letter character, a-z, after the @ sign in the email address. Basically ensuring that a letter is matched after the @ in the email and not a number or special character.
## Author

This turorial was created by Jasper Barcial

