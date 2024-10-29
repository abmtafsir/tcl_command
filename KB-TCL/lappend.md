# lappend

## Introduction:

The `lappend` command in Tcl is used to add elements to the end of a list. It allows us to modify lists by appending new elements to the existing list. If the list does not exist, the `lappend` command will create a new list with the specified elements. 

## Syntax:

`lappend varName ?value value ...?`


- `varName`: The name of the variable that holds the list to which elements will be appended.
- `value value ...`: One or more values to be appended to the list.

## Examples and Explanations:

### Example 1: Appending Single Element to an Existing List

**Code:**
``````
set my_list {apple banana}
lappend my_list orange
puts "Updated List: $my_list"
``````

**Output:**
``````
Updated List: apple banana orange
``````

In this example, we have an existing list "apple banana". We use the `lappend` command to append the element "orange" to the list. The list is modified, and the new list "apple banana orange" is obtained.

### Example 2: Appending Multiple Elements to an Existing List

**Code:**
``````
set my_list {apple banana}
lappend my_list orange mango
puts "Updated List: $my_list"
``````

**Output:**
``````
Updated List: apple banana orange mango
``````

In this example, we have an existing list "apple banana". We use the `lappend` command to append the elements "orange" and "mango" to the list. The list is modified, and the new list "apple banana orange mango" is obtained.

### Example 3: Creating a New List with `lappend`

**Code:**
``````
lappend new_list apple banana orange
puts "New List: $new_list"
``````

**Output:**
``````
New List: apple banana orange
``````

In this example, the `lappend` command is used without an existing list. The command creates a new list with the elements "apple banana orange", and the new list "apple banana orange" is obtained.


### Example 4: Appending List as an Element

**Code:**
``````
set my_list {apple banana}
lappend my_list {orange mango}
puts "Updated List: $my_list"
``````

**Output:**
``````
Updated List: apple banana {orange mango}
``````

In this example, we have an existing list "apple banana". We use the `lappend` command to append the list "{orange mango}" as a single element to the list. The list is modified, and the new list "apple banana {orange mango}" is obtained.

### Example 5: Appending Empty String

**Code:**
``````
set my_list {apple banana}
lappend my_list ""
puts "Updated List: $my_list"
``````

**Output:**
``````
Updated List: apple banana {}
``````

In this example, we have an existing list "apple banana". We use the `lappend` command to append an empty string as an element to the list. The list is modified, and the new list "apple banana {}" is obtained.

