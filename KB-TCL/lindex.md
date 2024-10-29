# lindex

## Introduction:

The `lindex` command in Tcl is used to access elements from a list. It allows us to retrieve a specific element from a list based on its index. List indices are 0-based, meaning the first element has an index of 0, the second element has an index of 1, and so on. 

## Syntax:

`lindex list ?index...`


- `list`: This is the input list from which you want to retrieve elements.
- `index...`: These are one or more indices specifying the elements you want to access. You can pass multiple indices to retrieve multiple elements at once.

## Examples and Explanations:

### Example 1:

**Code:**
``````
set my_list {apple banana orange}
set element [lindex $my_list 0]
puts "First element: $element"
``````

**Output:**
``````
First element: apple
``````

In this example, we have a list `apple banana orange` and we use the `lindex` command to access the first element, which has an index of 0. The first element `apple` is obtained.

### Example 2:

**Code:**
``````
set my_list {apple banana orange}
set element [lindex $my_list 2]
puts "Third element: $element"
``````

**Output:**
``````
Third element: orange
``````

In this example, we have a list `apple banana orange` and we use the `lindex` command to access the third element, which has an index of 2. The third element "orange" is obtained.

### Example 3:

**Code:**
``````
set my_list {1 2 3 4 5}
set element1 [lindex $my_list 1]
set element2 [lindex $my_list 3]
puts "Element at index 1: $element1"
puts "Element at index 3: $element2"
``````

**Output:**
``````
Element at index 1: 2
Element at index 3: 4
``````


In this example, we have a list `1 2 3 4 5` and we use the `lindex` command to access the elements at indices 1 and 3. The elements `2` and `4` at the respective indices are obtained.

### Example 4:

**Code:**
``````
set my_list {apple banana orange}
set elements [lindex $my_list 0 2]
puts "First and Third elements: $elements"
``````

**Output:**
``````
First and Third elements: apple orange
``````

In this example, we have a list `apple banana orange` and we use the `lindex` command to access the elements at indices 0 and 2 simultaneously. The elements `apple` and `orange` at the respective indices are obtained.

### Example 5:

**Code:**
``````
set my_list {1 2 3 4 5}
set element [lindex $my_list 6]
puts "Element at index 6: $element"
``````

**Output:**
``````
Element at index 6: 
``````

In this example, we have a list `1 2 3 4 5` and we attempt to access an element at index 6, which is beyond the range of the list. Since there is no element at index 6, an empty string is obtained.

