# Regex Tutorial

Welcome to this tutorial where we will delve deep into the structure and usage of JavaScript Regular Expressions (RegEx). We will construct an email validation RegEx, exploring various elements like anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes along the way.

## Summary

RegEx can be used to sort and locate many different things. One of the things it is commonly used for is validating email addresses. We''ll design a regex to validate an email address, the RegEx we'll be using is as follows:

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

### Anchors
In regex, anchors are used to specify the position of the pattern in relation to a line of text. There are two types of anchors: ^ and $. The caret ^ matches the pattern at the start of the line, while the dollar $ matches the pattern at the end of the line.

In our regex, we use both ^ at the beginning and $ at the end. This means the string must start and end with the given pattern.

### Quantifiers
Quantifiers determine how many times a character, group, or character class must appear for a match to be found. There are several quantifiers:

* Zero or more times
+ One or more times
? Zero or one times
{n} Exactly n times
{n,} At least n times
{n,m} At least n but not more than m times
In our regex, + means the preceding character or group (characters inside the brackets or parentheses) should appear at least once. {2,6} means the preceding character or group should appear at least 2 times but not more than 6 times.

### Grouping Constructs
Grouping constructs () are used to define the scope of operators and characters within them. They capture the text matched and allow us to use it later.

In our regex, we have three groups: ([a-z0-9_\.-]+), ([\da-z\.-]+), and ([a-z\.]{2,6}).

### Bracket Expressions
Bracket expressions [] define a character set where any character enclosed within the brackets can match a character at that position.

In our regex, [a-z0-9_\.-] means we are looking for any lower-case letter, digit, underscore, dot or hyphen.

### Character Classes
Character classes are specific pre-defined patterns. For example, \d matches any digit (same as [0-9]), \w matches any word character (same as [a-zA-Z0-9_]).

In our regex, \d in the second group represents any digit.

### The OR Operator
The pipe symbol | is used as an OR operator. It matches the pattern before or after it.

Our regex does not use this operator, but as an example, a|b would match either 'a' or 'b'.

### Flags
Flags change the search pattern. These include global (g), multiline (m), case-insensitive (i), etc.

Our regex does not use any flags, but for example, adding an 'i' at the end (/regex/i) would make the search case-insensitive.

### Character Escapes
The backslash \ is used to escape various characters including all metacharacters. For instance, to search for a period, you would need to escape it like this \..

In our regex, we escape the period character in \., since the period is a special character in regex, meaning 'any single character'.

So, the provided regex will check for an email address that starts and ends with the defined pattern, where the email name can contain any lower-case letter, digit, underscore, or dot.

## Author

Hailing from the sun-kissed sands of Huntington Beach, CA, I embarked on an adventurous journey that led me to graduate from the prestigious United States Naval Academy with a degree in Mechanical Engineering. My thirst for challenge saw me soaring the skies for six years as a Navy helicopter pilot, pushing the limits of machine and man. Now, grounded in the intensity of an ICU as a nurse, my sights are set on the digital frontier, aspiring to pivot into the riveting realm of software engineering.


