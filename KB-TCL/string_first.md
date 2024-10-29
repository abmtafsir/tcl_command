# string first

## Introduction:

The `string first` command in Tcl is used to find the index of the first occurrence of a substring within a given string. It allows us to locate the position of a specific substring in a string, which can be useful for various string manipulation tasks. It returns the index of the first character of the first occurrence of the substring. The search is case-sensitive, meaning it considers the characters' case during the search. If the `subString` is not found, the command returns `-1`. As it returns the index so its count starts from '0'. 

## Syntax:

The general syntax of the `string first` command is as follows:

`string first subString string ?startIndex?`

- `subString`: The substring you want to find within the given string.
- `string`: The input string in which you want to search for the substring.
- `startIndex`: (Optional) The starting index from where the search should begin. If not specified, the search starts from the beginning of the string.


## Examples and Explanations:

### Example 1: Finding the First Occurrence

**Code:**
``````
# Given string
set text "The quick brown fox jumps over the lazy dog."

# Find the index of the first occurrence of "fox"
set index [string first "fox" $text]

puts "Index of 'fox': $index"
``````

**Output:**
``````
Index of 'fox': 16
``````

In this example, we have a string variable `text` containing a sentence. We use the `string first` command to find the index of the first occurrence of the substring "fox" within the string. The command returns `16`, which is the index of the first character of the first occurrence of "fox" in the string.


### Example 2: Specifying a Starting Index


**Code:**
``````
# Given string
set sentence "I love coding, and I love learning new things."

# Find the index of the first occurrence of "love" after index 5
set startIndex 5
set index [string first "love" $sentence $startIndex]

puts "Index of 'love' after index $startIndex: $index"
``````

**Output:**
``````
Index of 'love' after index 5: 18
``````

In this example, we have a string variable `sentence` containing a sentence. We use the `string first` command and specify the `startIndex` as `5`, which means the search for `love` starts from index 5 (excluding the character at index 5). The command returns `18`, which is the index of the first character of the first occurrence of `love` after index 5 in the string.


### Example 3: Handling Non-Existent Substring

**Code:**
``````
# Given string
set message "Hello, World!"

# Find the index of the first occurrence of "abc"
set index [string first "abc" $message]

puts "Index of 'abc': $index"
``````

**Output:**
``````
Index of 'abc': -1
``````

In this example, we have a string variable `message` containing a message. We use the `string first` command to find the index of the first occurrence of the substring `abc` within the string. Since "abc" does not exist in the string, the command returns `-1` to indicate that the substring was not found.


