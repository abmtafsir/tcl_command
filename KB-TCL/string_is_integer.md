# string is integer

## Introduction

The `string is integer` command in Tcl is used to check whether a string represents a valid integer value. It returns a boolean value indicating whether the string can be successfully converted to an integer.

## Syntax:

`string is integer string`

- `string`: The string to be checked.

Return Value

- Returns `1` (true) if the string is a valid integer.
- Returns `0` (false) if the string is not a valid integer.

## Examples and Explanations

### Example 1: Check whether the value is an integer 

**Code:**

```
set num1 "123"

if {[string is integer $num1]} {
    puts "$num1 is a valid integer."
} else {
    puts "$num1 is not a valid integer."
}
```

**Output:**
```
123 is a valid integer.
```

In this example, the string `123` is a valid integer, and the `string is integer` command returns true. Therefore, the output is `123 is a valid integer.`

### Example 2:Check whether the value is not an integer 

**Code:**

```
set num2 "abc"

if {[string is integer $num2]} {
    puts "$num2 is a valid integer."
} else {
    puts "$num2 is not a valid integer."
}
```
**Output:**

```
abc is not a valid integer.
```

In this example, the string `abc` is not a valid integer because it contains non-numeric characters. Hence, the `string is integer` command returns false. Therefore, the output is `abc is not a valid integer.`

### Example 3: Float is not an integer

**Code:**

```
set num3 "987.65"

if {[string is integer $num3]} {
    puts "$num3 is a valid integer."
} else {
    puts "$num3 is not a valid integer."
}
```
**Output:**
```
987.65 is not a valid integer.
```

In this example, the string `987.65` is not a valid integer because it contains a decimal point. The `string is integer` command only accepts whole numbers without any fractional part. Hence, it returns false. Therefore, the output is `987.65 is not a valid integer.`


