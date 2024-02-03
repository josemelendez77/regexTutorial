# Regular expressions

Regular expressions, commonly known as regex, denote a specific string composed of diverse character sets. They serve as both a querying tool and a validator in code bases and traditional documents. Originating from the concept of regular language introduced by mathematician Stephen Cole Kleene, regular expressions gained widespread adoption within the field of theoretical computer science. They provide a means to match patterns within text files and facilitate lexical analysis.

Despite their reputation for appearing cryptic, a closer examination reveals that regular expressions are not as intricate as they might seem at first glance. Breaking them down piece by piece unveils their underlying structure, making it relatively straightforward for individuals to start crafting their own regex expressions.

## Summary

In this guide, we'll delve into a regular expression designed to both match and validate email addresses:

^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$
Imagine you're a software developer on a mission to identify insecurely used email addresses scattered throughout a codebase. By employing the above regular expression, you can swiftly locate all instances of emails in the codebase and other documents. This regex expression isn't just useful for searching; it can also be integrated as a string in a codebase to ensure that users input valid email addresses. When users fill out forms requiring a valid email, incorporating this regex string mandates a specific format: a set number of characters, followed by an "@" symbol, a domain name of a specified length, and a domain name system (e.g., .com, .net, .dev) ranging between 2 and 6 characters.

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
The elements that define this specific regular expression include anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expressions. In the context of the tutorial's example, the anchors ^ and $ are employed, quantifiers + and {2, 6} are used, \d represents the meta escape character, character classes are denoted by [a-z0-9_.-], [\da-z.-], and [a-z.], single character matches include _, ., and -, grouping and capturing are represented by (), and a bracket expression is enclosed within [].

### Anchors
In regular expressions, anchors designate the beginning and conclusion of an expression. Specifically, within this expression, the ^ symbolizes the start, while the $ signifies the end.
### Quantifiers 
Quantifiers serve as metacharacters that alter the behavior of the preceding character or character class in a regular expression, indicating how many consecutive occurrences are sought.

These metacharacters provide a way to define the quantity of characters or character classes to be matched. The + symbol, for instance, matches one or more of the preceding character, while {min, max} establishes a specific numerical range for the quantifier. In the given regex expression, this range is employed at the end to specify the range for the domain name system.

### OR Operator
This specific regex expression doesn't include OR operators. However, in general, OR operators are denoted by the pipe symbol | and fall under the category of alternation in regex.

### Character Classes
Character classes in a regex expression define specific sets of characters for a search pattern. In this regex expression, the character classes employed include [a-z0-9_.-], [\da-z.-], and [a-z.].
[a-z0-9_.-]:
a-z matches a single character in the range between 'a' (index 97) and 'z' (index 122) (case-sensitive).
0-9 matches a single digit character in the range between '0' (index 48) and '9' (index 57) (case-sensitive).
_ matches the underscore character literally (case-sensitive).
. matches the dot character '.' literally (case-sensitive).
matches the hyphen character '-' literally (case-sensitive).
[\da-z.-]:
\d matches any digit (0-9).
a-z matches a single character in the range between 'a' (index 97) and 'z' (index 122) (case-sensitive).
. matches the dot character '.' literally (case-sensitive).
matches the hyphen character '-' literally (case-sensitive).
[a-z.]:
a-z matches a single character in the range between 'a' (index 97) and 'z' (index 122) (case-sensitive).
. matches the dot character '.' literally (case-sensitive).
Other examples of single characters in regex include:
\d to match any digit (0-9).
\w to match any alphanumeric character (a-zA-Z0-9).
\s to match any white space, such as a space or tab.
### Flags
Regex flags in JavaScript are employed to modify the behavior of an expression, such as controlling case sensitivity. In JavaScript, there are six flags:

i: Enables case-insensitive matching.
g: Looks for all matches in the provided text.
m: Activates multiline mode, affecting the behavior of ^ and $.
s: Enables "dotall" mode, allowing a dot (.) to match newline characters (\n).
u: Provides full Unicode support.
y: Activates "sticky" mode for matching.
It's important to note that the regex expression discussed in this tutorial does not incorporate any flags.
### Grouping and Capturing
The use of parentheses () in a regular expression serves to create a sequence or subexpression, treating multiple characters as a single unit. In the regex expression discussed in this tutorial, parentheses are employed to define distinct groups of characters. The first set encompasses all characters before the '@' symbol. The second group encompasses all characters before the '.', and the last group encompasses all characters from the '.' to the end.
### Bracket Expressions
Square brackets [] in a regular expression define a character or group range, representing a single character. In the context of the regex expression discussed in this tutorial, square brackets are utilized to delineate each character class. The character can be any specified within the brackets.
For instance, in the example [a-z0-9_.-], a character can be matched with any lowercase letters from 'a' to 'z', a digit from '0' to '9', an underscore '_', a period '.', or a dash '-'.
### Greedy and Lazy Match
Greedy matching, the default behavior in regex, involves the regex engine attempting to match as much of the string as possible. In contrast, lazy matching seeks to match as little of the string as possible.
Key distinctions:

Greedy matching continues searching until the specified condition is met.
Lazy matching stops searching as soon as the condition is satisfied.
It's essential to note that greedy matching can be slower than lazy matching because it persists until the end of the string, exploring all possible matches. In contrast, lazy matching halts upon finding the first match.

### Back-references
Back-references are instructions that point to a previous segment of the matched regular expression. Typically, they are denoted by a backslash followed by a single digit, such as \2.

### Look-ahead and Look-behind

Look-ahead, often denoted as ?=foo, captures the content immediately following the string "foo." On the other hand, look-behind, indicated as ?<=foo, captures the content that immediately precedes the string "foo."
## Author
Jose melendez is cuurently a software enginner who wants to get involved with the change in tech. He wants to encounter problems never seen before and solve them with his own education. He currently resides in Salt Lake City.
 
 Github: https://github.com/josemelendez77/josemelendez77
 Email: melendezjose585@gmail.com

