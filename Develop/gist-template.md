# Regex Tutorial

Regular Expression, or Regex for short, is simply a way of seaching for data. Using a sequence of characters that specifies a search pattern.\
For example: ``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  ```
\
This will search for any pattern that matches what these chararcters have specified. Hard to believe but this sequence is searching for any email that is possible. Let's break it down

## Summary

In this tutorial we are going to cover what goes into a Regular expression and what makes them work. Specifically, we are going to go through and see how this sequence of code (below) functions at all.

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```

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
When writing a Regular Expression one needs to first allow the computer to know that we are starting a regex. This is where Anchors come in. Anchors do not match to a character but match a position before or after the characters.\
```^ ``` - The caret matches to the beginning of the regex text.\
```$ ```- The dollar sign matches to the end of the text.


### Quantifiers
Quantifiers specify how mayn instances of a character, group, or character class must be present for a match to be made/found.\
Quantififiers in this regex epxression includes the ```+``` operator. This will connect the user's email name + email sercive + .com.
Yet another quantifier is ```{2,6}``` which will allow a match of 2-6 characters for the character set of ```[a-z\.]```


### OR Operator
The OR (read as or not O.R.) Operator is also refered to as Alternation. It is simply a way to add a "or" into your search sequence. This code does not have it, but it is written with a single vertical line character ```|```.
A simple example would be\
```I love CSS|HTML``` this would match ```I love HTML``` or ```I love CSS```

### Character Classes
Character Class also known as Character set. It is simply a specical notation that matches any symbol from a certain set. 
for example: ```[A-Z]``` will match any UPPERCASE letter in the English Alphabet.\
```/d``` will match any digit that is 0-9. This will only come back with a single digit like "6" and not "666"
### Flags
Flags are tokens that modify its behavior of searching. They are optional parameters that we can add to an expression to make it search differently. 

```i``` stands for ignore casing, makeing a search case-insensitive.\
```g``` stands for global this allows the search to extend to more than just one match.


### Grouping and Capturing

Capturing groups is a way to treat mulitple characters as a single unit. This is done with the parenthesis ```()``` It is a good way to create a block of patterns so that you can apply repitions or other modifiers to them as a whole. 
```([a-z0-9_\.-]+)``` matches the email's username. 
```([\da-z\.-]+)``` matches the email's service/
```([a-z\.]{2,6})``` matches the .com

### Bracket Expressions

Bracket Expressions are a list of characters and/or character classes enclosed in brackets ```[]``` 
Use the bracket expression to match single characters in a list, or a rance of characters in list. 

### Greedy and Lazy Match
A greedy match matches to as many characters as possible. Meaning it will find every character you tell it to. 
Whereas the Lazy match will match to the shortest string possible.

In our example we do include a greedy match as the sequence has a ```+``` Quantifier.
Another greedy Quantifier used in this regex is ```{}``` when matching ```{2,6}``` for the last capture group.


### Boundaries
Boundary Matchers make matches more precise by specifying certain information. With boundaries you can search for characters at the beginning of a line, end of a line, word boundary, non-word boundary, and more. 

### Back-references
Back References are regular expressions commands which refer to a previous part of the matched regex. They are specified with a blackslash ```\``` 

for example, in our code ```a-z0-9_\``` is looking for the exact same text again.

### Look-ahead and Look-behind
Look ahead and Look behing allow us to find matches that are followed or preceded by another pattern. 
Look ahead syntax is ```X(?=Y)``` this is saying look for X but only match if followed by Y
Look behing has both a postivie look behind and a negative look behind. This dictates in which way the secondary value is in relation to the first.
Positive lookbehind: ```(?<=Y)X```, matches X, but only if there’s Y before it.
Negative lookbehind: ```(?<!Y)X```, matches X, but only if there’s no Y before it.


## Author

 GitHub: <a href = 'https://github.com/AaronCox73'> AaronCox73 </a>
  Email: <a href = 'mailto:Aaronjeffersoncox@gmail.com'> Aaronjeffersoncox@gmail.com </a>
