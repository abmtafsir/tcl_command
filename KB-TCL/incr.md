# incr

## Introduction:

The `incr` command in Tcl is used to increment the value of a variable by a specified amount. It provides a convenient way to update the value of a variable in-place. The `incr` command is commonly used for counting, iteration, and various numerical operations. It adds the specified `increment` value to the current value of the variable `varName`. If the `increment` value is not provided, the default increment is `1`. The `incr` command allows you to modify the variable directly without having to assign the updated value explicitly.

## Syntax:

The general syntax of the `incr` command is as follows:

`incr varName ?increment?`


- `varName`: The name of the variable to be incremented.
- `increment`: (Optional) The value by which the variable will be incremented. If not specified, the default value is `1`.

## Examples and Explanations:

Let's go through some examples to illustrate the usage of the `incr` command:

### Example 1: Increment by 1 (Default)

**Code:**
``````
# Initialize a variable
set count 0

# Increment the variable by 1 (default)
incr count

puts "Updated count: $count"
``````

**Output:**
``````
Updated count: 1
``````

In this example, we have a variable named `count` initialized to `0`. We use the `incr` command without specifying an `increment` value, which means the variable `count` is incremented by the default value of `1`. The `puts` command then displays the updated value of `count`, which is `1`.

### Example 2: Increment by a Specific Amount

**Code:**
``````
# Initialize a variable
set value 10

# Increment the variable by a specific amount (e.g., 5)
incr value 5

puts "Updated value: $value"
``````

**Output:**
``````
Updated value: 15
``````

In this example, we have a variable named `value` initialized to `10`. We use the `incr` command and specify the `increment` value as `5`. The variable `value` is then incremented by `5`, resulting in the updated value of `15`.

### Example 3: Using `incr` with a Loop

**Code:**
``````
# Initialize a variable
set sum 0

# Increment the variable using a loop
for {set i 1} {$i <= 5} {incr i} {
    incr sum $i
}

puts "Sum: $sum"
``````

**Output:**
``````
Sum: 15
``````

In this example, we have a variable `sum` initialized to `0`. We use a `for` loop to increment the variable `sum` by the loop index `i` ranging from `1` to `5`. After the loop, the value of `sum` will be the sum of numbers from `1` to `5`, which is `15`.
