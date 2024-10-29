# lreplace

## Introduction:

The `lreplace` command in Tcl is used to replace elements in a list with new elements. It allows us to modify specific elements in a list while keeping the rest of the list intact. 

## Syntax: 

`lreplace list first last ?element element ...?`

- `list`: The name of the list in which elements will be replaced.
- `first`: The index of the first element to be replaced.
- `last`: The index of the last element to be replaced.
- `element element ...`: One or more elements to replace the specified range of elements.


## Examples and Explanations:

### Example 1: Replacing Elements in a List

**Code:**
``````
set my_list {apple banana orange}
set new_list [lreplace $my_list 1 2 pear mango]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple pear mango
``````

In this example, we have a list "apple banana orange". We use the `lreplace` command to replace elements at indices 1 and 2 with the elements "pear" and "mango". The new list "apple pear mango" is obtained while keeping the rest of the list intact.

### Example 2: Replacing a Single Element

**Code:**
``````
set my_list {apple banana orange}
set new_list [lreplace $my_list 1 1 pear]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple pear orange
``````

In this example, we replace the element at index 1 in the list "apple banana orange" with the element "pear". The new list "apple pear orange" is obtained.

### Example 3: Replacing a Range with an Empty Element

**Code:**
``````
set my_list {apple banana orange}
set new_list [lreplace $my_list 1 2]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple orange
``````

In this example, we replace the elements at indices 1 and 2 in the list "apple banana orange" with an empty range of elements. The new list "apple orange" is obtained.

### Example 4: Replacing Multiple Elements

**Code:**
``````
set my_list {apple banana orange}
set new_list [lreplace $my_list 0 1 pear mango kiwi]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: pear mango kiwi orange
``````

In this example, we replace the elements at indices 0 and 1 in the list "apple banana orange" with the elements "pear", "mango", and "kiwi". The new list "pear mango kiwi orange" is obtained.

### Example 5: Replacing Elements in a Nested List

**Code:**
``````
set nested_list {{apple banana} {orange kiwi}}
set new_list [lreplace $nested_list 0 1 {grape pineapple}]
puts "Original List: $nested_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: {apple banana} {orange kiwi}
New List: {grape pineapple}
``````

In this example, we replace the sublists at indices 0 and 1 in the nested list "{{apple banana} {orange kiwi}}" with the sublist "{grape pineapple}". The new nested list "{{grape pineapple} {orange kiwi}}" is obtained.

