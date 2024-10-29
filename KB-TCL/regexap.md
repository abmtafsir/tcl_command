# regexp

## Introduction:

The `regexp` command in Tcl is used for pattern matching using regular expressions. Regular expressions are powerful tools for matching and manipulating strings based on specific patterns. The `regexp` command allows you to search for patterns in strings, extract substrings based on patterns, and perform various string manipulations. The `regexp` command searches the `string` for occurrences of the `pattern`. The `pattern` is a sequence of characters that define the matching criteria using regular expression syntax. Regular expressions consist of special characters and metacharacters that represent patterns, repetitions, alternatives, and more.

When `regexp` finds a match, it returns `1`, and if no match is found, it returns `0`. If the `matchVar` is provided, the matched substring will be stored in that variable. If there are any capturing groups in the `pattern`, the substrings matched by those groups will be stored in the `subMatchVar` variables.


## Syntax:

The general syntax of the `regexp` command is as follows:

`regexp ?switches? pattern string ?matchVar? ?subMatchVar ...?`


- `switches`: (Optional) Specifies various options for pattern matching.
- `pattern`: The regular expression pattern to be matched.
- `string`: The input string to search for matches.
- `matchVar`: (Optional) The variable to store the matched substring.
- `subMatchVar`: (Optional) Variables to store submatches (captured groups) from the pattern.



## Example and Explanation:

Let's go through some examples to illustrate the usage of the `regexp` command:

### Example 1: Basic Pattern Matching

**Code:**
``````
# Given string
set text "Hello, Tcl is awesome!"

# Check if the string contains "Tcl"
if {[regexp "Tcl" $text]} {
    puts "Found 'Tcl' in the string."
} else {
    puts "'Tcl' not found in the string."
}
``````

**Output:**
``````
Found 'Tcl' in the string.
``````

In this example, we have a string variable `text`. We use the `regexp` command to check if the string contains the substring "Tcl". Since "Tcl" is present in the string, the command returns `1`, and the message "Found 'Tcl' in the string." is displayed.

### Example 2: Using Capturing Groups

**Code:**
``````
# Given string
set sentence "I love coding in Tcl."

# Extract the word after "love"
regexp {love (\w+)} $sentence -> word

puts "Word after 'love': $word"
``````

**Output:**
``````
Word after 'love': coding
``````

In this example, we have a string variable `sentence`. We use the `regexp` command with a capturing group `(\w+)` to extract the word (not any symbol) that comes after "love" in the sentence. The matched word "coding" is stored in the variable `word`.


### Example 3: Using Case-Insensitive Matching

**Code:**
``````
# Given string
set data "apples and Apples are delicious."

# Check if the string contains "apples" (case-insensitive)
if {[regexp -nocase "apples" $data]} {
    puts "Found 'apples' (case-insensitive) in the string."
} else {
    puts "'apples' (case-insensitive) not found in the string."
}
``````

**Output:**
``````
Found 'apples' (case-insensitive) in the string.
``````

In this example, we have a string variable `data`. We use the `-nocase` switch with the `regexp` command to perform a case-insensitive search for the substring "apples" in the string. The command finds "apples" (ignoring the case), and the message "Found 'apples' (case-insensitive) in the string." is displayed.
