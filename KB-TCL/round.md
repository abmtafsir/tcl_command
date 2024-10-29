# round

## Introduction

The `round` function in Tcl is used to round a floating-point number to the nearest integer value according to the rounding rules. It returns the closest whole number based on the specified precision.

## Syntax

`round number ?precision?``


- `number`: The floating-point number to be rounded.
- `precision` (optional): The number of decimal places to round to. If not specified, the default precision is 0.

Return Value

- Returns the rounded integer value.

## Example and Explanation

### Example 1:

**Code:**
``````
set value 3.7
set roundedValue [round $value]

puts "Value: $value"
puts "Rounded Value: $roundedValue"
``````
**Output:**
``````
Value: 3.7
Rounded Value: 4
``````
In this example, the floating-point number `3.7` is rounded to the nearest whole number using the `round` function. Since `3.7` is closer to `4` than to `3`, the rounded value is `4`.

### Example 2:

**Code:**
``````
set value 5.2
set roundedValue [round $value]

puts "Value: $value"
puts "Rounded Value: $roundedValue"
``````
**Output:**
``````
Value: 5.2
Rounded Value: 5
``````
In this example, the floating-point number `5.2` is rounded to the nearest whole number using the `round` function. Since `5.2` is closer to `5` than to `6`, the rounded value is `5`.

### Example 3:

**Code:**
``````
set value 9.99
set roundedValue [round $value 1]

puts "Value: $value"
puts "Rounded Value: $roundedValue"
``````
**Output:**
``````
Value: 9.99
Rounded Value: 10.0
``````

In this example, the floating-point number `9.99` is rounded to one decimal place using the `round` function with a precision of `1`. The rounded value is `10.0`, indicating one decimal place precision.

