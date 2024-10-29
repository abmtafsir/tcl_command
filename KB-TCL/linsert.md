# linsert

## Introduction:
The `linsert` command in Tcl is used to insert elements into a list at a specified index position. It allows us to add new elements to a list without replacing existing elements. 

## Syntax:

`linsert list index ?element element ...?`


- `list`: The name of the list into which elements will be inserted.
- `index`: The index position at which the elements will be inserted. Use `end` to insert at the end of the list.
- `element element ...`: One or more elements to be inserted at the specified index.

## Examples and Explanations:

### Example 1: Inserting an Element at the Beginning of the List


**Code:**
``````
set my_list {apple banana orange}
set new_list [linsert $my_list 0 pear]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: pear apple banana orange
``````

In this example, we have a list `apple banana orange`. We use the `linsert` command to insert the element "pear" at index 0. The new list `pear apple banana orange` is obtained.

### Example 2: Inserting Elements in the Middle of the List


**Code:**
``````
set my_list {apple banana orange}
set new_list [linsert $my_list 1 pear mango]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple pear mango banana orange
``````

In this example, we insert the elements `pear` and `mango` at index 1 in the list `apple banana orange`. The new list `apple pear mango banana orange` is obtained.

### Example 3: Inserting Elements at the End of the List

**Code:**
``````
set my_list {apple banana orange}
set new_list [linsert $my_list end pear mango]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple banana orange pear mango
``````

In this example, we use the `end` keyword to insert the elements `pear` and `mango` at the end of the list `apple banana orange`. The new list `apple banana orange pear mango` is obtained.

### Example 4: Inserting Elements in a Nested List

**Code:**
``````
set nested_list {{apple banana} {orange kiwi}}
set new_list [linsert $nested_list 1 grape pineapple]
puts "Original List: $nested_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: {apple banana} {orange kiwi}
New List: {apple banana} grape pineapple {orange kiwi}
``````

In this example, we insert the elements `rape` and `pineapple` at index 1 in the nested list `{{apple banana} {orange kiwi}}`. The new nested list `{{apple banana} grape pineapple {orange kiwi}}` is obtained.

### Example 5: Inserting a List as an Element

**Code:**
``````
set my_list {apple banana orange}
set new_list [linsert $my_list 1 {pear mango}]
puts "Original List: $my_list"
puts "New List: $new_list"
``````

**Output:**
``````
Original List: apple banana orange
New List: apple {pear mango} banana orange
``````

In this example, we insert the list `{pear mango}` as a single element at index 1 in the list `apple banana orange`. The new list `apple {pear mango} banana orange` is obtained.

