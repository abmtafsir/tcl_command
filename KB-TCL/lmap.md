# lmap

### Introduction:

The `lmap` command in Tcl is used to apply a script or expression to each element of a list and generate a new list containing the results. It allows us to transform the elements of a list in a concise and efficient manner. 

S## yntax:

`lmap varName list script`


- `varName`: The variable name used to refer to each element of the list.
- `list`: The input list.
- `script`: The script or expression to be applied to each element.

## Examples and Explanations:

### Example 1: Transforming Elements

**Code:**
``````
set numbers {1 2 3 4}
set squared_numbers [lmap x $numbers {expr {$x * $x}}]
puts "Original Numbers: $numbers"
puts "Squared Numbers: $squared_numbers"
``````

**Output:**
``````
Original Numbers: 1 2 3 4
Squared Numbers: 1 4 9 16
``````

In this example, we use the `lmap` command to square each element of the list "1 2 3 4". The expression `{expr {$x * $x}}` calculates the square of each number, and the result is a new list containing the squared numbers.

### Example 2: Manipulating Strings

**Code:**
``````
set names {"Alice" "Bob" "Charlie"}
set name_lengths [lmap name $names {string length $name}]
puts "Names: $names"
puts "Name Lengths: $name_lengths"
``````

**Output:**
``````
Names: Alice Bob Charlie
Name Lengths: 5 3 7
``````

In this example, we use the `lmap` command to calculate the length of each name in the list "Alice Bob Charlie". The script `string length $name` calculates the length of each name, and the result is a new list containing the name lengths.

### Example 3: Filtering Elements

**Code:**
``````
set numbers {1 2 3 4 5 6}
set even_numbers [lmap x $numbers {if {$x % 2 == 0} then {set x} else {}}]
puts "Original Numbers: $numbers"
puts "Even Numbers: $even_numbers"
``````

**Output:**
``````
Original Numbers: 1 2 3 4 5 6
Even Numbers: {} 2 {} 4 {} 6
``````

In this example, we use the `lmap` command to filter out the even numbers from the list "1 2 3 4 5 6". The script checks if each number is even using the condition `$x % 2 == 0` and includes the even numbers in the result list.

