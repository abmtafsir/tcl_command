# proc

## Introduction:

In Tcl, `proc` is used to define procedures or user-defined commands. Procedures are reusable blocks of code that can be called multiple times throughout a program. They help in organizing code, improving readability, and reducing redundancy. A `proc` command allows you to create custom functions that can be called by their names, passing arguments to them.

## Syntax:

The general syntax for defining a `proc` in Tcl is as follows:
``````
proc procedureName {args} {
    body
}
``````

- `procedureName`: The name of the procedure that you want to define.
- `args`: A list of arguments that the procedure takes (if any).
- `body`: The code to be executed when the procedure is called.

## Examples and Explanations:

### Example 01: Define a procedure to add two numbers

Let's go through a simple example to illustrate the usage of the `proc` command:

**Code:**
``````
# Define a procedure
proc addNumbers {num1 num2} {
    set sum [expr {$num1 + $num2}]
    return $sum
}

# Call the procedure with arguments

set result [addNumbers 5 7]
puts "Result: $result" ;
``````
**Output:**
`````` 
Result: 12
``````

In this example, we define a procedure named `addNumbers` that takes two arguments `num1` and `num2`. Inside the procedure, we calculate their sum using the `expr` command and store it in the variable `sum`. The `return` command is used to return the result to the caller.

We then call the `addNumbers` procedure with arguments `5` and `7`. The procedure calculates the sum, and the result is stored in the variable `result`, which is printed as "Result: 12".



### Example 02: Procedures with Default Values


Tcl allows you to define default values for procedure arguments. If a value is not provided for an argument during the procedure call, the default value will be used. Here's an example:

**Code:**
``````
# Define a procedure with default values
proc greetUser {name {greeting "Hello"}} {
    puts "$greeting, $name!"
}

# Call the procedure with and without providing the second argument
greetUser "Alice" ;
``````
**Output:** 
``````
Hello, Alice!
greetUser "Bob" "Hi" ;
``````

**Output:** 
``````
Hi, Bob!
``````

In this example, we define a procedure `greetUser` that takes two arguments: `name` and `greeting` (with a default value of "Hello"). If the `greeting` argument is not provided during the procedure call, it will use the default value "Hello". When the `greetUser` procedure is called with only one argument, it uses the default greeting "Hello". When called with two arguments, it uses the provided greeting.


### Example 03: Returning Multiple Values:

Tcl allows procedures to return multiple values by using the `return` command with a list of values. Here's an example:

**Code:**
``````
# Define a procedure to calculate the sum and product of two numbers
proc math_operations {num1 num2} {
    set sum [expr {$num1 + $num2}]
    set product [expr {$num1 * $num2}]
    return [list $sum $product]
}

# Call the procedure and retrieve the result as a list
set result [math_operations 3 4]
puts "Sum: [lindex $result 0], Product: [lindex $result 1]" ;
``````
**Output:** 
``````
Sum: 7, Product: 12
``````

In this example, the `mathOperations` procedure calculates the sum and product of two numbers `num1` and `num2`. It returns the results as a list using the `return` command. The caller retrieves the results as a list and accesses individual values using the `lindex` command.

### Example 04: Access Variable That Defined Outside The Proc

**Code:**
```
# Declare a variable outside the proc
set myVar 42

# Define a proc that uses the variable
proc myProc {} {
    # Access the variable declared outside the proc
    global myVar
    puts "Value of myVar inside the proc: $myVar"
}

# Call the proc
myProc
```

**Output:**
```
Value of myVar inside the proc: 42
```