# lrange
## Introduction:

The `lrange` command in Tcl is used to extract a sub-list from a given list. It allows us to specify a range of indices to create a new list containing the selected elements. 

## Syntax:

`lrange list start end`


- `list`: The original list.
- `start`: The index of the first element to include.
- `end`: The index of the last element to include.

## Examples and Explanations:

### Example 1: Extracting a Range of Elements

**Code:**
``````
set my_list {apple banana orange grape}
set sub_list [lrange $my_list 1 2]
puts "Original List: $my_list"
puts "Sub-List: $sub_list"
``````

**Output:**
``````
Original List: apple banana orange grape
Sub-List: banana orange
``````

In this example, we extract a sub-list containing elements from index 1 to 2 (inclusive) from the original list "apple banana orange grape". The result is "banana orange".

### Example 2: Extracting the First N Elements

**Code:**
``````
set my_list {apple banana orange grape}
set sub_list [lrange $my_list 0 2]
puts "Original List: $my_list"
puts "Sub-List: $sub_list"
``````

**Output:**
``````
Original List: apple banana orange grape
Sub-List: apple banana orange
``````

In this example, we extract a sub-list containing the first three elements (index 0 to 2) from the original list "apple banana orange grape". The result is "apple banana orange".

### Example 3: Extracting the Last N Element:

**Code:**
``````
set my_list {apple banana orange grape}
set sub_list [lrange $my_list end-2 end]
puts "Original List: $my_list"
puts "Sub-List: $sub_list"
``````

**Output:**
``````
Original List: apple banana orange grape
Sub-List: orange grape
``````

In this example, we extract a sub-list containing the last two elements from the original list "apple banana orange grape" using the "end" index notation. The result is "orange grape".

### Example 4: Extracting a Single Element

**Code:**
``````
set my_list {apple banana orange grape}
set sub_list [lrange $my_list 2 2]
puts "Original List: $my_list"
puts "Sub-List: $sub_list"
``````

**Output:**
``````
Original List: apple banana orange grape
Sub-List: orange
``````
In this example, we extract a sub-list containing a single element at index 2 from the original list "apple banana orange grape". The result is "orange".
