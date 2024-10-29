# string tolower and string toupper

## Introduction 

The `string tolower` and `string toupper` commands in Tcl are used to convert the case of characters in a string. 

- `string tolower`: Converts all uppercase characters in a string to lowercase.
- `string toupper`: Converts all lowercase characters in a string to uppercase.

## Syntax

The syntax of `string tolower` and `string toupper` is as follows:

`string tolower string`

`string toupper string`


- `string`: The input string that you want to convert the case of.

## Examples and Explanations

### Example 1: Converting a String to Lowercase

**Code:**
```
set sentence "Hello, World!"
set lowercaseSentence [string tolower $sentence]

puts "Original String: '$sentence'"
puts "Lowercase String: '$lowercaseSentence'"
```

**Output:**

```
Original String: 'Hello, World!'
Lowercase String: 'hello, world!'
```


In this example, the `sentence` variable contains the input string `Hello, World!`. The `string tolower` command is used to convert all the uppercase characters in the string to lowercase. The resulting lowercase string is stored in the `lowercaseSentence` variable.

### Example 2: Converting a String to Uppercase

**Code:**
```
set sentence "Hello, World!"
set uppercaseSentence [string toupper $sentence]

puts "Original String: '$sentence'"
puts "Uppercase String: '$uppercaseSentence'"
```

**Output:**
```
Original String: 'Hello, World!'
Uppercase String: 'HELLO, WORLD!'
```

In this example, the `sentence` variable contains the input string `Hello, World!`. The `string toupper` command is used to convert all the lowercase characters in the string to uppercase. The resulting uppercase string is stored in the `uppercaseSentence` variable.

