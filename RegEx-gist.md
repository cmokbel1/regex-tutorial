## RegEx Email Validation Tutorial 

Hello and welcome to the email validation RegEx Tutorial. Today you will learn some cool things about RegEx and how it can be used to validate user inputs to make sure your server is receiving the appropriate information.

## Summary

I will be detailing how one can validate e-mail input from users to ensure the information the server is receiving is actually an e-mail and not just some random string that was hastily input. One can reference this snippet to better understand how this tutorial will go -> ``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```

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
  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
### Anchors
the '^' is known as a caret and is the primary anchor which matches the beginning of the string or the start of a line if the multiline flag (m) is enabled. Secondly, the '@' caret is rather self-explanatory in that it matches the @ symbol that accompanies an e-mail. Third is the '$' caret which matches the end of a string or the end of a line if the multiline flag (m) is enabled.
### Quantifiers
 A quantifier is a symbol that is input to match 1 or more a preceding character or token. examples of quanitifers are symbols such as, '+'. `[a-z0-9_\.-]` the '+' here will match a hyphen if there is one. Quantifiers can also include ranges set between a pair of curly braces {}. for instance near the end of the code snippet the quanitifer {2,6} means there can be a minimum of 2 or maximum of 6 characters including and between a - z.
### Grouping Constructs
Grouping constructs are used to separate portions of characters that are in relation to each other. standard group constructs are paraenthesis. () the account name is contained within the first () -> `([a-z0-9_\.-]+)`. the Website is contained within the second set of grouping constructs `([\da-z\.-]+)`. and the final portion of the website commonly '.com' is contained within the final grouping construct `([a-z\.]{2,6})`
### Bracket Expressions
Bracket expressions are used to help define character sets. they are simply '[]'. Whatever comes between these brackets is considered a character set and used to define parameters for allowed characters.
### Character Classes
Character classes include characters that can be found throughout the code snippet above. 

A 'Literal Character' is any character that does not include `^`,`-`, `]`, or `\`. the `_` in `[a-z0-9_\.-]` matches an _ character should it be present in the string. 

A 'Backslash' escapes special characters to suppress their special meaning. in this bit of code `[a-z0-9_\.-]` the escaped character of . removes the meaning found outside of a bracket expression and allows it to be passed in with the string.

A 'Range' is defined by using a hyphen between two tokens that each sepcificy a single character. These ranges can include the two tokens that are used as boundaries. `[a-z0-9_\.-] `a-z matches a character between a and z. the 0-9 range matches any character within that range. 

\d displayed `([\da-z\.-]+)` matches any digit from 0-9.
### The OR Operator
'+' , '*'. In this code snippet the OR operator '+' means it will match 1 or more of the bracketed character sets. `([a-z0-9_\.-]+`
### Flags
This code snippet does not use any flags. Flags are tokens that modify the behavior of searches. They are optional. for example the `g` flag searches for all matches of a given expression inside a string instead of stopping in the first match.
### Character Escapes
Character escapes were discussed earlier in the character classes section. However, to reiterate, in this code snippet the `\` is used to negate any special meaning a character may have outside of the given representation. characters such as `.` serve a different purpose outside of their negation with a backslash. similarly, a caret `^` is used to match the beginning of a string but when used with a backslash means to not include a specific range or character.
## Author

My name is Claude. I'm a newer developer based out of Southern California. I have high hopes and the discipline to match these hopes. I intend on becoming a senior developer some day and also intend on beginning my own coding company in the future. To the moon we go!!!!!!!!!!!!!!!!!!!!!!
