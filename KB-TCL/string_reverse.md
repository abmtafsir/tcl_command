# string reverse

## Introduction

The `string reverse` command in Tcl is used to reverse the order of characters in a string. It takes a string as input and returns a new string with the characters reversed.


## Syntax

The syntax of the `string reverse` command is as follows:

`string reverse string`


- `string`: The input string that you want to reverse.


## Examples and Explanations

### Example 1: Reversing a Simple String

**Code:**
```
set sentence "Hello, World!"
set reversedSentence [string reverse $sentence]

puts "Original String: '$sentence'"
puts "Reversed String: '$reversedSentence'"
```

**Output:**
```
Original String: 'Hello, World!'
Reversed String: '!dlroW ,olleH'
```

In this example, the `sentence` variable contains the input string `Hello, World!`. The `string reverse` command is used to reverse the order of characters in the string. The resulting reversed string is stored in the `reversedSentence` variable.

### Example 2: Reversing a Numeric String

**Code:**
```
set number "12345"
set reversedNumber [string reverse $number]

puts "Original Number: '$number'"
puts "Reversed Number: '$reversedNumber'"
```

**Output:**
```
Original Number: '12345'
Reversed Number: '54321'
```

In this example, the `number` variable contains the numeric string `12345`. The `string reverse` command is used to reverse the order of digits in the string. The resulting reversed number is stored in the `reversedNumber` variable.

