# string range


## Introduction:

The `string range` command in Tcl is used to extract a substring from a given string. It allows you to select a range of characters from the input string based on the starting and ending indices. 

## Syntax:

`string range string start end`


- `string`: This is the input string from which you want to extract the substring.
- `start`: This is the starting index (inclusive) of the substring. The index is 0-based, meaning the first character has index 0, the second character has index 1, and so on.
- `end`: This is the ending index (inclusive) of the substring. If you want to extract a single character, `end` should be the same as `start`.

## Examples and Explanations:

### Example 1:


**Code:**
``````
set str "Hello, World!"
set subStr [string range $str 0 4]
puts "Substring: $subStr"
``````

**Output:**
``````
Substring: Hello
``````

In this example, we have a string `Hello, World!` and we use the `string range` command to extract a substring starting from index 0 and ending at index 4 (inclusive). The substring `Hello` is obtained.

### Example 2:

**Code:**
``````
set str "Tcl is a simple scripting language."
set subStr [string range $str 4 5]
puts "Substring: $subStr"
``````

**Output:**
``````
Substring: is
``````

In this example, we have a string `Tcl is a simple scripting language.` and we use the `string range` command to extract a substring starting from index 4 and ending at index 5 (inclusive). The substring `is` is obtained.

### Example 3:


**Code:**
``````
set str "Tcl is fun!"
set subStr [string range $str 8 9]
puts "Substring: $subStr"
``````

**Output:**
``````
Substring: un
``````

In this example, we have a string `Tcl is fun!` and we use the `string range` command to extract a substring starting from index 8 and ending at index 9 (inclusive). The substring `un` is obtained.

### Example 4:

**Code:**
``````
set str "Tcl is awesome!"
set subStr [string range $str 4 end]
puts "Substring: $subStr"
``````

**Output:**
``````
Substring: is awesome!
``````

In this example, we have a string `Tcl is awesome!` and we use the `string range` command to extract a substring starting from index 4 and going up to the end of the string. The `end` keyword is used to represent the last index of the string. The substring `is awesome!` is obtained.

### Example 5:


**Code:**
``````
set str "Tcl is versatile."
set subStr [string range $str 0 end-3]
puts "Substring: $subStr"
``````

**Output:**
``````
Substring: Tcl is versatile
``````

In this example, we have a string `Tcl is versatile.` and we use the `string range` command to extract a substring starting from index 0 and going up to the third character from the end of the string (index `end-3`). The substring `Tcl is versatile` is obtained.


