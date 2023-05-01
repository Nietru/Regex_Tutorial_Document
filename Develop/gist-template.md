# Moderate Password Strength Regex

In this assignment, I was given the task of selecting one commonly used Regex to create a tutorial for.

## Summary

```
I decided to go with the Password complexity: Moderate Regex.
This should match a string that contains 1 lowercase letter, 1 uppercase letter, 1 number, and be atleast 8 characters long.
In general, regular expressions allow you to search through text in your code, in an advanced way. They allow us to match strings with specific patterns.
Most regexes can be written in multiple ways and are not always the same for different programming languages and frameworks.
```

## Table of Contents

- [Meta Characters and Anchors](#meta-characters-and-anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

(?=(._[0-9]))((?=._[A-Za-z0-9])(?=._[A-Z])(?=._[a-z]))^.{8,}$

```
This JavaScript regex checks if a given input, like a password, meets the following requirements:

    At least one digit (0-9)
    At least one uppercase letter (A-Z)
    At least one lowercase letter (a-z)
    At least 8 characters long

The pattern makes sure the input is complex enough by enforcing these rules.
```

```
This JavaScript regular expression is used to validate the format of a given input string, typically for password strength validation. Let's break down the regex pattern to understand each part:

   (?=(.[0-9])): This is a positive lookahead assertion that checks for the presence of at least one digit (0-9) in the input string. The expression inside the parentheses (.[0-9]) means any character (.) followed by a digit [0-9]. The lookahead assertion doesn't consume the characters, which means it only checks if the condition is met without moving the regex engine's position.

   ((?=.[A-Za-z0-9])(?=.[A-Z])(?=._[a-z])): This is a group of three positive lookahead assertions combined. They check for the presence of:
       At least one alphanumeric character (A-Z, a-z, 0-9) with the pattern (._[A-Za-z0-9])
       At least one uppercase letter (A-Z) with the pattern (._[A-Z])
       At least one lowercase letter (a-z) with the pattern (._[a-z])

   ^.{8,}$: This part checks if the input string has at least 8 characters in length. The caret (^) indicates the start of the string, and the dollar sign ($) indicates the end of the string. The dot (.) represents any character, and {8,} means a minimum of 8 repetitions of the preceding character.

In summary, this regex pattern checks if the input string (typically a password) has at least 8 characters, including at least one digit, one uppercase letter, one lowercase letter, and one alphanumeric character. This is a common pattern used to enforce password complexity rules.
```

### Meta Characters and Anchors

Anchors represent the matching position of a string of characters.

1.  \d -> Indicates any digit, one character 0-9.
2.  \w -> Indicates any word, any character that you might find as part of a word, letter or number: A-Z a-z 0-9.
3.  \s -> Whitespace.
    Note: if you were to do a capital \D, it would be anything that ISNT a digit. Same with \W and \S
    (represents the opposite)
4.  . -> ANY character what-so-ever! Unless inside of brackets.
5.  The ^ symbol anchor represents the beginning of a string.
6.  The $ symbol anchor represents the end of a string.
7.  the \b anchor represents a word boundary.

### Quantifiers

```
Quantifiers help us match one or more characters in a row, as opposed to single meta characters.
example: We can find all 5 letter words like so: \s\w{5}\s
            The \s represents a white-space, and the \w represents a word. These are single meta characters, but the {5} is the quantifier.
```

1.  - -> 0 or more.
2.  - -> 1 or more.
3.  ? -> 0 or 1.
4.  {min, max}
5.  {n} (show in the above example)

### Bracket Expressions

```
In JavaScript regex, bracket expressions [...] let you match one character from a set of characters. You can define ranges like [0-9] for digits, [a-z] for lowercase letters, or [A-Z] for uppercase letters. You can also list individual characters, like [aeiou] for vowels. Use [^...] to match any character except those in the set.
```

### Character Classes

```
In JavaScript regular expressions, character classes are predefined shorthand notations to represent specific sets of characters. They make regex patterns more concise and easier to read. Here are some common character classes in JavaScript:

    \d: Matches any digit (0-9). Equivalent to [0-9].
    \D: Matches any non-digit character. Equivalent to [^0-9].
    \w: Matches any alphanumeric character (A-Z, a-z, 0-9) and the underscore (_). Equivalent to [A-Za-z0-9_].
    \W: Matches any non-alphanumeric character, except for the underscore. Equivalent to [^A-Za-z0-9_].
    \s: Matches any whitespace character (spaces, tabs, line breaks). Includes spaces, tabs, and newline characters.
    \S: Matches any non-whitespace character.

These character classes help simplify regex patterns by replacing longer bracket expressions with a single character. For example, instead of writing [0-9] to match a digit, you can use \d.
```

### The OR Operator

```
In JavaScript regex, the | symbol is the OR operator. It lets you match multiple patterns in a single expression. example: /cat|dog/ matches either "cat" or "dog".
```

```
Use parentheses ( ) to group patterns
example: /(apple|banana|strawberry)/, which matches "apple", "banana", or "strawberry".
```

### Flags

```
In JavaScript regular expressions, flags are single-letter options that modify the behavior of the regex pattern. They are placed after the closing delimiter / of the regex pattern. Here are the most common flags in JavaScript regex:
```

1.  g (global) -> Searches for all matches in the input string, rather than stopping at the first match.
2.  i (ignore case) -> Makes the regex pattern case-insensitive, so it matches characters regardless of their case.
3.  m (multiline) -> Treats the input string as multiple lines, allowing the ^ and $ anchors to match the start and end of each line, rather than just the start and end of the entire string.
4.  s (dotAll) -> Makes the dot . special character match any character, including newline characters, which it normally doesn't match.
5.  u (unicode) -> Treats the pattern as a Unicode pattern, allowing you to work with Unicode characters and astral symbols correctly.
6.  y (sticky) -> Searches for a match starting exactly at the current position (defined by the lastIndex property) in the input string, instead of searching from the beginning.

You can use multiple flags together by placing them after the regex pattern.

### Character Escapes

```
In JavaScript regex, character escapes use a backslash \ to give special characters a literal meaning or to represent specific characters. For example:

    \\: Matches a backslash \.
    \.: Matches a dot . literally.
    \d: Matches any digit (0-9).
    \s: Matches any whitespace character (spaces, tabs, line breaks).
    \n: Matches a newline character.

Character escapes help you represent special characters or give literal meaning to meta-characters in your regex patterns.
```

## Author

I am Tifannie Truman, and am currently enrolled in the full-stack web development course through the Univerity of New Hampshire. I aspire to become a full-stack junior developer once further along in my learning journey!
Github: https://github.com/Nietru
LinkedIn: https://www.linkedin.com/in/nietru143/
