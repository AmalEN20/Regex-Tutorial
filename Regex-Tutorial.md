# Title (replace with your title)

Regex is short for regular expression which is a string of text to help search for or sometimes vaildate input text. It can be used in varies programming language such as Javascript and search engines such as Ctrl+F function in Google Docs. In this explaining a "simple" regex that matches for a any vaild email.

## Summary

Here is the code snipet of matching an Email in Regex: 
 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

To quickly describe this Regex expression, it's looking for any character group of varying size and characters, followed by the '@' symbol, followed by another varying character group, followed by a period '.', and end with a group of character with a minimum of 2 but up to 6 characters. I created this to be a useful guide for students such as myself to reference by explain what each section of code does and what each part is defined as. (Anchors, Quantifiers, Character Classes, etc..)


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
1. `^randomtext$` 
- exact string match from start '^' to end '$' which is "randomtext" with this example

### Quantifiers
1. `+` 
- matches a string that has 1 or more of the previous character or sequence
2. `{2,6}` 
- matches a string that has at least 2 but up to 6 copies of the previous character or sequence

### Character Classes
1. `\d` 
- matches any single character that is a digit or 'number' from 0 to 9
- its similar as using '0-9'
2. `\.` 
- this is literal meta char for "."
- '\' changes the period to become literal character instead of being a Greedy Operaters that matches as many characters as possible
3. `@` 
- this is literal character for '@'
- unlike the period before, '@' doesn't have any special operation associated with it so it does need the backlash '\' before it


### Grouping and Capturing
1. `([a-z0-9_\.-]+)` 
2. `([\da-z\.-]+)` 
- matches any grouping of one or more characters that are a-z, 0-9, a underscore '_', an literal period '.', or a hyphen '-' 
- this also shows a use case for the Quanifier '+' mentioned earlier to increase the size of the match for the group
3. `([a-z\.]{2,6})` 
- matches any grouping of at least 2 but up to 6 characters that are a-z or an literal period '.'
- this shows a use case for the Quanifier '{2,6}' mentioned earlier to increase the size of the match for the group

### Bracket Expressions
1. `[a-z0-9_\.-]` 
2. `[\da-z\.-]`
- both matches any single character that's a-z, 0-9, a underscore '_', an literal period '.', or a hyphen '-' 
3. `[a-z\.]`
- matches any single character that's a-z or an literal period '.'


## Author
Amal Engulatov - Full Stack Web Developer
[Link to my GitHub Profile] (https://github.com/AmalEN20)