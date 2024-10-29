# string equal

## Introduction

The `string equal` command in Tcl is used to compare two strings for equality. It checks if two strings have the same characters and length, returning a boolean value indicating the result.

## Syntax

The syntax of the `string equal` command is as follows:

`string equal string1 string2 ?-nocase?`


- `string1` and `string2`: The strings to be compared.
- `-nocase`: (Optional) Specifies that the comparison should be case-insensitive.

## Examples and Explanations

### Example 1: Comparing Two Equal Strings


**Code:**
``````
set string1 "Hello"
set string2 "Hello"

if {[string equal $string1 $string2]} {
    puts "The strings are equal."
} else {
    puts "The strings are not equal."
}
``````

**Output:**
``````
The strings are equal.
``````

In this example, the `string1` and `string2` variables contain the strings `Hello`. The `string equal` command is used to compare the two strings. Since both strings have the same characters and length, the condition `[string equal $string1 $string2]` evaluates to true, and the message `The strings are equal.` is printed.


Caution: 

	1. invalid bareword "string" it means [] bracket is needed in between strings equal str1 and str2.
	2. The white space also need to be equal. Such as:
	
	set sen1 "my name is tafsir"
	puts "sentence1: $sen1"
	
	set sen2 " my name is tafsir "
	puts "sentence2: $sen2"
	
Here `sen1` and `sen2` will not be equal because of the white spaces in sen2 at the beginning and at the end. 





### Example 2: Comparing Two Different Strings

**Code:**

``````
set string1 "Hello"
set string2 "World"

if {[string equal $string1 $string2]} {
    puts "The strings are equal."
} else {
    puts "The strings are not equal."
}
``````

**Output:**
``````
The strings are not equal.
``````

In this example, the `string1` variable contains the string "Hello", and the `string2` variable contains the string "World". The `string equal` command is used to compare the two strings. Since the strings have different characters or lengths, the condition `[string equal $string1 $string2]` evaluates to false, and the message `The strings are not equal.` is printed.


### Example 3: Case-Insensitive Comparison


**Code:**
``````
set string1 "Hello"
set string2 "hello"

if {[string equal $string1 $string2 -nocase]} {
    puts "The strings are equal (case-insensitive)."
} else {
    puts "The strings are not equal (case-insensitive)."
}
``````

**Output:**
``````
The strings are equal (case-insensitive).
``````

In this example, the `string1` variable contains the string "Hello", and the `string2` variable contains the string "hello". The `-nocase` option is used with the `string equal` command to perform a case-insensitive comparison. Since the option is specified, the condition `[string equal $string1 $string2 -nocase]` evaluates to true, and the message `The strings are equal (case-insensitive).` is printed.

