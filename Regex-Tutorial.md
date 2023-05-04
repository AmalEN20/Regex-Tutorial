# Regex Tutorial

Regex is short for regular expression which is a string of text to help search for or sometimes vaildate input text. It can be used in varies programming language such as Javascript and search engines such as Ctrl+F function in Google Docs. In this explaining a "simple" regex that matches for a any vaild email.

## Summary

Here is the code snipet of matching an Email in Regex: 
 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

To quickly describe this Regex expression, it's looking for any character group of varying size and characters, followed by the '@' symbol, followed by another varying character group, followed by a period '.', and end with a group of character with a minimum of 2 but up to 6 characters. I created this to be a useful guide for students such as myself to reference by explain what each section of code does and what each part is defined as. (Anchors, Quantifiers, Character Classes.)


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

- `^` You can use the caret symbol `(^)` at the end of a regular expression to indicate that a match must occur at the beginning of the searched text matches at the beginning of the target string
- `$` You can use the dollar symbol `($)` at the start of a regular expression to indicate that a match must occur at the text ending of content or text searched

`/^[content]$/`


^abc$	start / end of the string

The caret `^` matches the position before the first character in the string. Applying `^a` to `abcd` matches `a`. ^b and ^c does not match `abcd` at all, because the b and c cannot be matched right after the start of the string, matched by `^`. See below for the inside view of the regex engine.
Similarly, `$` matches right after the last character in the string. `d$` matches `d` in abc, while a$ does not match at all.

In regular expressions, anchors mark the beginning and end of a string, line, or word. The beginning of the email string is marked by `^` and the end is marked by `$`.
/^[content]$/
A start of a new line of string would be marked by `^` and ended with a `$`

### Quantifiers

/`^`([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]{2,6})`$`/  <br>
 - `*`   representing `0` or more occurrences of the atom,
 - `+`   representing `1` or more occurrence of the atom,
 - `?`   representing `0` or `1` occurrences of the atom,
 - the bound `{n}`   representing exactly n occurrences of the atom,
 - the bound `{m,n}`   representing between m and n occurrences of the atom.

When we used `+` to communicate there should be another sequence to be matched as a greedy quantifier.  Example `{n,m}` or `{3,9}` as another greedy quantifer to specify the input should be a minimum of `2` characrtors to a maximum of `9` characters.

This regex uses two different types of quantifiers. The first can be found in two places
`([a-z0-9_\.-]+)`
`([a-z\.]{2,6})`

### Character Classes
/^([a-z0-9_\`.`-]+)@([`\d`a-z\`.`-]`+`)\.(`[a-z\`.`]`{2,6})$/  <br>
In this Regex, the charactor class `/d` is used which in Javasctipt classifies the use of any digit from `0` to `9`.


### Grouping and Capturing

/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/ <br>
There are 3 groups being captured in this example. The charactor class `/d` in 1st Group is the username of the email account `[A-Za-z0-9_\.-]` ~ "McNoor2022". The 2nd group captures the domain name or e-mail service being used `[\da-z\.-]` ~"@.gmail" Lastly, the 3rd group captures the domain extention (i.e .com or .net and .usabcd) `[a-z\.]{2,6}`

### Bracket Expressions
/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/
Similar to groups in this example, there are also 3 bracket expressions. The information in the bracket expressions is opened and closed between brackets like this `[]`. This indentifies which information is allowed to be matched.

For example 	`[Me]`+`[eE]` matches `me`, `mE`, `Me`, and `ME`.
`gr[ae]y` matches both spellings of the word `'grey'`; that is, `gray` and `grey`.

Bracket Expression first: `[A-Za-z0-9_\.-]` - includes non-case sensitive characters from a-z, numbers from 0-9 an underscore, periods and hyphens.

Bracket Expression second: `[\da-z\.-]`   - includes all digits, case sensitive characters from a-z, periods and hyphens

Bracket Expression third: `[a-z\.]`      - includes case sensitive characters from a-z and periods.

### Greedy and Lazy Match
/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/  <br>
Here, we have only used greedy quantifiers `+` and `{}`, meaning that it will allow the match to expand as long as it neess to go. If these quantifiers were non-greedy quantifiers, they would appear as `+?` or `{}?`, this will direct the system to make the shortest match.


## Author
Amal Engulatov - Full Stack Web Developer
[Link to my GitHub Profile] (https://github.com/AmalEN20)
