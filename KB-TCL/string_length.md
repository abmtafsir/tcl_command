# string length

## Introduction:

The `string length` command in Tcl is used to find the length of a given string. It returns the number of characters (including spaces and special characters) in the string. 

## Syntax:

`string length string`


- `string`: This is the input string for which you want to find the length.

## Examples and Explanations:

### Example 1:

**Code:**
```
set str "Hello, World!"
set length [string length $str]
puts "The length of the string is: $length"
```

**Output:**
```
The length of the string is: 13
```

In this example, we have a string "Hello, World!" and we use the `string length` command to find its length, which is 13 characters.

### Example 2:

**Code:**
```
set str "Tcl is a simple scripting language."
set length [string length $str]
puts "The length of the string is: $length"
```

**Output:**
```
The length of the string is: 33
```

In this example, we have a string `Tcl is a simple scripting language.` and we use the `string length` command to find its length, which is 33 characters.

### Example 3:

**Code:**
```
set emptyStr ""
set length [string length $emptyStr]
puts "The length of the empty string is: $length"
```

**Output:**
```
The length of the empty string is: 0
```

In this example, we have an empty string `""`, and we use the `string length` command to find its length, which is 0 because there are no characters in the empty string.

### Example 4:

**Code:**
```
set str "   Spaces   "
set length [string length $str]
puts "The length of the string is: $length"
```

**Output:**
```
The length of the string is: 12
```

In this example, we have a string `   Spaces   ` that contains spaces at the beginning and end. The `string length` command counts all the characters, including the spaces, so the length is 12.

### Example 5: VVI 

**Code:**
```
set str "Tcl is fun!"
set subStr [string range $str 0 2]
set length [string length $subStr]
puts "The length of the substring is: $length"
```

**Output:**
```
The length of the substring is: 3
```

In this example, we first extract a substring `Tcl` from the original string `Tcl is fun!` using the `string range` command. Then, we use the `string length` command to find the length of this substring, which is 3 characters.


