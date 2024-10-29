# set

## Introduction:

The `set` command in Tcl is used to create and manipulate variables. Variables are used to store data that can be accessed and modified throughout the program. The `set` command allows us to assign values to variables and retrieve those values when needed. 

## Syntax:

`set varName ?value?`


- `varName`: The name of the variable.
- `value`: (Optional) The value to be assigned to the variable.

## Examples and Explanations:

### Example 1: Creating and Assigning Values to Variables

**Code:**
``````
set name "Alice"
set age 25
``````

In this example, the `set` command is used to create two variables, `name` and `age`, and assign values to them. The variable `name` is assigned the value "Alice," and the variable `age` is assigned the value 25.

### Example 2: Retrieving Variable Values

**Code:**
``````
set fruit "apple"
puts "The selected fruit is: $fruit"
``````

**Output:**
``````
The selected fruit is: apple
``````

In this example, the value of the variable `fruit` is retrieved and displayed using the `puts` command. The value is accessed using the syntax `$variableName`.

### Example 3: Updating Variable Values

**Code:**
``````
set counter 0
puts "Counter: $counter"
set counter [expr $counter + 1]
puts "Updated Counter: $counter"
``````

**Output:**
``````
Counter: 0
Updated Counter: 1
``````

In this example, the variable `counter` is initially set to 0. The value is displayed using the `puts` command. Then, the value of `counter` is updated using an expression (`[expr $counter + 1]`), and the updated value is displayed.

## Example 4: Variable Interpolation

**Code:**
``````
set x 5
set y 3
set result [expr $x + $y]
puts "$x + $y = $result"
``````

**Output:**
``````
5 + 3 = 8
``````

In this example, the variables `x` and `y` are used in an expression to calculate the sum. The result is stored in the variable `result`. The `puts` command displays the values of `x`, `y`, and the result in the form of an equation.

## Example 5: Value undervalue

**Code:**
``````
puts "Give first value"
gets stdin p1
puts "The first value is $p1"
puts "Give second value"
gets stdin p2
puts "The second value is $p2"
set a {p1 p2}
set length [llength $a]
set b [expr int ((rand () * $length))]
set c [lindex $a $b]
puts "The value under value us [set $c]"
``````
**Output:**
``````
Give first value
taf
The first value is taf
Give second value
sir
The second value is sir
The value under value us sir
``````