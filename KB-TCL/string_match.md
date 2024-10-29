# string match

## Introduction
 
The `string match` command in Tcl is used to perform pattern matching and determine if a string matches a specified pattern. It compares the string against the pattern and returns a boolean value indicating whether there is a match or not.


## Syntax

The syntax of the `string match` command is as follows:

`string match pattern string`


- `pattern`: The pattern to match against.
- `string`: The string to be matched.


**Patterns**

Patterns in Tcl are specified using a combination of literal characters and special pattern-matching characters. The following pattern-matching characters can be used:

- `*`: Matches any sequence of characters, including an empty string.
- `?`: Matches any single character.
- `[set]`: Matches any single character from the set specified inside the square brackets.
- `[^set]`: Matches any single character not present in the set specified inside the square brackets.


## Examples and Explanations

### Example 1: Basic Pattern Matching

**Code:**
```
set string "Hello, World!"

if {[string match "Hello*" $string]} {
    puts "The string matches the pattern."
} else {
    puts "The string does not match the pattern."
}
```

**Output:**
```
The string matches the pattern.
```

In this example, the `string` variable contains the string "Hello, World!". The `string match` command is used to check if the string matches the pattern "Hello*". The `*` character in the pattern matches any sequence of characters, so the condition `[string match "Hello*" $string]` evaluates to true, and the message "The string matches the pattern." is printed.

### Caution:

Let's take a closer look at the `string match` command and the pattern used in the given code snippet.

The `string match` command in Tcl is used for pattern matching with the help of wildcard characters. The asterisk (*) is one such wildcard character that represents "zero or more occurrences of the previous character or pattern."

**In the given code snippet:**
```
set string "Hello, World!"

if {[string match "World*" $string]} {
    puts "The string matches the pattern."
} else {
    puts "The string does not match the pattern."
}
```

The pattern used is `World*`. This pattern specifies that the string should start with the literal string `World` followed by zero or more characters. The asterisk (*) indicates that any number of characters can occur after "World" or no characters at all.

However, in the given string `Hello, World!`, the substring `World` is not at the beginning of the string. It is preceded by the substring `Hello, `. Since the pattern `World*` requires the string to start with `World`, it does not match the given string.

To illustrate this, let's consider another example:

**Code:**
```
set string "World of Warcraft"

if {[string match "World*" $string]} {
    puts "The string matches the pattern."
} else {
    puts "The string does not match the pattern."
}
```

**Output:**
```
The string matches the pattern.
```

In this example, the given string is `World of Warcraft`. Since the string starts with `World`, it matches the pattern `World*`. The output is `The string matches the pattern.`

In summary, the original code snippet's output states that the string does not match the pattern because the pattern `World*` expects the string to start with `World`, while the given string `Hello, World!` does not fulfill this requirement.


### Example 2: Pattern Matching with Character Set


**Code:**

```
set string "apple"

if {[string match {[aeiou]*} $string]} {
    puts "The string matches the pattern."
} else {
    puts "The string does not match the pattern."
}
```

**Caution: Here the pattern is in between {}** 

**Output:**
```
The string matches the pattern.
```

In this example, the `string` variable contains the string `apple`. The `string match` command is used to check if the string matches the pattern `[aeiou]*`. The `[aeiou]` character set in the pattern matches any single vowel character, and the `*` character matches any sequence of characters. Since the string starts with a vowel ("a"), the condition `[string match "[aeiou]*" $string]` evaluates to true, and the message `The string matches the pattern.` is printed.


### Example 3: Exact String Match


**Code:**

```
set string "Tafsir"

if {[string match "Tafsir" $string]} {
    puts "The string matches the pattern."
} else {
    puts "The string does not match the pattern."
}
```

**Output:**
```
The string matches the pattern.
```

In this example, the `string` variable contains the string `Tafsir`. The `string match` command is used to check if the string matches the pattern `Tafsir` exactly. Since the string is an exact match to the pattern, the condition `[string match "Tafsir" $string]` evaluates to true, and the message `The string matches the pattern.` is printed.
