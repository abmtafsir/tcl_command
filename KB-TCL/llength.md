# llength

## Introduction:

The `llength` command in Tcl is used to determine the number of elements in a list. It allows you to quickly obtain the length of a list, which is the count of elements it contains. 

## Syntax:

`llength list`

- `list`: The name of the list whose length you want to find.

## Examples and Explanations:

### Example 1: Finding the Length of a List


**Code:**
``````
set my_list {apple banana orange}
set length [llength $my_list]
puts "Length of the list: $length"
``````

**Output:**
``````
Length of the list: 3
``````

In this example, we have a list "apple banana orange", and we use the `llength` command to determine its length. The length of the list, which is the count of elements it contains (3), is obtained.

### Example 2: Handling Empty List

**Code:**
``````
set empty_list {}
set length [llength $empty_list]
puts "Length of the empty list: $length"
``````

**Output:**
``````
Length of the empty list: 0
``````

In this example, we have an empty list, and we use the `llength` command to determine its length. Since the list is empty, the length is 0.

### Example 3: Counting Elements in a Nested List

**Code:**
``````
set nested_list {{1 2 3} {4 5} {6 7 8 9}}
set length [llength $nested_list]
puts "Length of the nested list: $length"
``````

**Output:**
``````
Length of the nested list: 3
``````

In this example, we have a nested list containing three sublists. We use the `llength` command to determine the length of the outer list, which is the count of sublists it contains (3).


### Example 4: Finding Length of List Elements


**Code:**
``````
set list_of_strings {"apple banana" "orange mango" "kiwi"}
foreach element $list_of_strings {
    set length [llength $element]
    puts "Length of '$element': $length"
}
``````

**Output:**
``````
Length of 'apple banana': 2
Length of 'orange mango': 2
Length of 'kiwi': 1
``````

In this example, we have a list of strings, and we use a `foreach` loop to iterate through each element. We use the `llength` command to determine the length of each element, which is the count of words in the string.

