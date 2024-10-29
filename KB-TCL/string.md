# string

## Introduction:

The `string` command in Tcl provides a range of operations and manipulations for working with strings. It allows us to perform tasks such as string comparison, formatting, modification, extraction, and more. The `string` command is a versatile tool for string manipulation within Tcl scripts. 

## Syntax:

`string option ?arg...?`

- `option`: The specific operation to perform on the string.
- `arg...`: (Optional) Additional arguments required for the specified operation.

## Examples and Explanations:

**Example 1: String Length**

**Code:**

```
set text "Hello, World!"
set length [string length $text]
puts "Length of text: $length"
```


**Output:**
``````
Length of text: 13
``````

In this example, the `string length` operation is used to determine the length of the string "Hello, World!" The result is stored in the variable `length`, and the length is printed using the `puts` command.

**Example 2: String Comparison**

**Code:**

``````
set str1 "apple"
set str2 "banana"
if {[string equal $str1 $str2]} {
    puts "Strings are equal."
} else {
    puts "Strings are not equal."
}
``````

**Output:**

``````
Strings are not equal.
``````

In this example, the `string equal` operation is used to compare two strings, `str1` and `str2`. Since the strings are not equal, the output message indicates that the strings are not equal.

**Example 3: String Extraction**

**Code:**

``````
set sentence "The quick brown fox"
set word [string range $sentence 4 8]
puts "Extracted word: $word"
``````

**Output:**

``````
Extracted word: quick
``````

In this example, the `string range` operation is used to extract a substring from the string "The quick brown fox." The substring is defined by the indices 4 and 8, resulting in the word "quick."

**Example 4: String Formatting**

**Code:**

``````
set name "Alice"
set age 30
set formatted [string format "Name: %s, Age: %d" $name $age]
puts $formatted
``````

**Output:**

``````
Name: Alice, Age: 30
``````

In this example, the `string format` operation is used to create a formatted string. The placeholders `%s` and `%d` are replaced with the values of the variables `name` and `age`, respectively.


