# lset
## Introduction:

The `lset` command in Tcl is used to modify the value at a specific index within a list. It allows us to update a specific element of a list, making it a powerful tool for manipulating lists in Tcl.

## Syntax:

The general syntax of the `lset` command is as follows:

`lset listName ?index1 ... indexN? newValue`

- `listName`: The name of the list to be modified.
- `index1 ... indexN`: One or more indices representing the path to the desired element within the list.
- `newValue`: The new value to be assigned at the specified index.


## Example and Explanation:


### Example 1:

**Code:**
``````
set myList {1 2 3 4}
puts "Original List: $myList"

lset myList 1 5
puts "Modified List: $myList"
``````

**Output:**
``````
Original List: 1 2 3 4
Modified List: 1 5 3 4
``````

In this example, we have a list named `myList` with initial values `{1 2 3 4}`. Using the `lset` command, we modify the value at index `1` (which is the second element in the list) to `5`. After modifying the list, the new value is reflected in the output.


**Nested List Modification:**

The `lset` command can also be used to modify elements within nested lists. 

### Example 2:

**Code**
``````
set nestedList {{1 2} {3 4}}
puts "Original Nested List: $nestedList"

lset nestedList 0 1 5
puts "Modified Nested List: $nestedList"
``````

**Output:**
``````
Original Nested List: {1 2} {3 4}
Modified Nested List: {1 5} {3 4}
``````

In this example, we have a nested list named `nestedList` with initial values `{{1 2} {3 4}}`. Using the `lset` command with two indices, we modify the value at index `0 1` (the second element of the first sublist) to `5`. The modified list is then printed, showing the updated value.
