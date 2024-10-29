# split

## Introduction 

The `split` command in Tcl is used to split a string into a list of substrings based on a specified delimiter. It allows you to break a string into smaller parts based on a specific pattern or character.

## Syntax

The syntax of the `split` command is as follows:

`split string ?splitChars?`


- `string`: The input string to be split.
- `splitChars`: (Optional) The delimiter or characters used for splitting the string. If not specified, the default delimiter is a space character.


## Examples and Explanations

### Example 1: Splitting a String by Space

**Code:**
``````
set sentence "Hello, World! How are you?"
set words [split $sentence]

foreach word $words {
    puts $word
}
``````

**Output:**
``````
Hello,
World!
How
are
you?
``````

In this example, the `sentence` variable contains the input string "Hello, World! How are you?". The `split` command is used without specifying any `splitChars`, so the default delimiter (space) is used. The string is split into individual words, and each word is printed using a `foreach` loop.

### Example 2: Splitting a String by a Custom Delimiter

**Code:**
``````
set sentence "apple,banana,grape,orange"
set fruits [split $sentence ","]

foreach fruit $fruits {
    puts $fruit
}
``````

**Output:**
``````
apple
banana
grape
orange
``````

In this example, the `sentence` variable contains the input string "apple,banana,grape,orange". The `split` command is used with a custom delimiter (`,`). The string is split into individual fruits based on the delimiter, and each fruit is printed using a `foreach` loop.



