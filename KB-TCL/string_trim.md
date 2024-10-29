# string trim


## Introduction

The `string trim` command in Tcl is used to remove leading and trailing whitespace characters from a string. It allows you to eliminate unwanted spaces, tabs, or newlines from the beginning and end of a string.


## Syntax

The syntax of the `string trim` command is as follows:

`string trim? string? ?chars?`


- `string`: The input string from which you want to remove leading and trailing whitespace. This argument is optional. If not provided, an empty string will be used.
- `chars`: A string containing the characters that you want to remove from the beginning and end of the input string. This argument is optional. If not provided, the default behavior is to remove all whitespace characters (spaces, tabs, and newlines).


## Examples and Explanations

### Example 1: Removing Whitespace from a String

**Code:**
``````
set sentence "   Hello, World!   "
set trimmedSentence [string trim $sentence]

puts "Original String: '$sentence'"
puts "Trimmed String: '$trimmedSentence'"
``````

**Output:**
``````
Original String: '   Hello, World!   '
Trimmed String: 'Hello, World!'
``````

In this example, the `sentence` variable contains a string with leading and trailing spaces. The `string trim` command is used to remove the whitespace characters from the beginning and end of the string, resulting in the trimmed string being stored in the `trimmedSentence` variable.

### Example 2: Removing Specific Characters from a String


**Code:**
``````
set sentence "---Hello, World!---"
set trimmedSentence [string trim $sentence "-"]

puts "Original String: '$sentence'"
puts "Trimmed String: '$trimmedSentence'"
``````

**Output:**
``````
Original String: '---Hello, World!---'
Trimmed String: 'Hello, World!'
``````

In this example, the `sentence` variable contains a string with leading and trailing dashes. The `string trim` command is used to remove the dashes from the beginning and end of the string by specifying the `-` character as the `chars` argument. The resulting trimmed string is stored in the `trimmedSentence` variable.


### Example 3: Remove White Space Within a String

**Code:**
``````
set sentence "Hello,     World!"
set trimmedSentence [string trim [string map {" " ""} $sentence]]

puts "Original String: '$sentence'"
puts "Trimmed String: '$trimmedSentence'"
``````
**Output:**
``````
Original String: 'Hello,     World!'
Trimmed String: 'Hello,World!'
``````
In this example the sentence `Hello,  World` is stored in the sentence variable. The `string map` cut off the space in between `Hello,` and `World!` and stored in `trimmedSentence`


