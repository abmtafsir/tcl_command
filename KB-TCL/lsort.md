# lsort

## Introduction:

The `lsort` command in Tcl is used to sort the elements of a list in ascending or descending order. It can also sort lists based on various options, such as dictionary order, numeric order, and unique elements. 

## Syntax:

`lsort ?options? list`

- `options`: Optional sorting options.
- `list`: The list to be sorted.

## Examples and Explanations:

#### Example 1: Sorting in Ascending Order

**Code:**
``````
set my_list {apple banana orange}
set sorted_list [lsort $my_list]
puts "Original List: $my_list"
puts "Sorted List (Ascending): $sorted_list"
``````

**Output:**
``````
Original List: apple banana orange
Sorted List (Ascending): apple banana orange
``````

In this example, we sort the list "apple banana orange" in ascending order using the `lsort` command. The result is "apple banana orange".

### Example 2: Sorting in Descending Order

**Code:**
``````
set my_list {apple banana orange}
set sorted_list [lsort -decreasing $my_list]
puts "Original List: $my_list"
puts "Sorted List (Descending): $sorted_list"
``````

**Output:**
``````
Original List: apple banana orange
Sorted List (Descending): orange banana apple
``````

In this example, we sort the list "apple banana orange" in descending order using the `lsort` command with the                       `-decreasing` option. The result is "orange banana apple".

### Example 3: Sorting in Numeric Order

**Code:**
``````
set num_list {20 5 100 10}
set sorted_list [lsort -integer $num_list]
puts "Original List: $num_list"
puts "Sorted List (Numeric Order): $sorted_list"
``````

**Output:**
``````
Original List: 20 5 100 10
Sorted List (Numeric Order): 5 10 20 100
``````

In this example, we sort the numeric list "20 5 100 10" in numeric order using the `-integer` option of the `lsort` command. The result is "5 10 20 100".

### Example 4: Sorting in Dictionary Order

**Code:**
``````
set dict_list {apple11 apple2 apple20}
set sorted_list [lsort -dictionary $dict_list]
puts "Original List: $dict_list"
puts "Sorted List (Dictionary Order): $sorted_list"
``````

**Output:**
``````
Original List: apple11 apple2 apple20
Sorted List (Dictionary Order): apple2 apple11 apple20
``````

In this example, we sort the list "apple11 apple2 apple20" in dictionary order using the `-dictionary` option of the `lsort` command. The result is "apple2 apple11 apple20".

### Example 5: Sorting with Unique Elements

**Code:**
``````
set duplicate_list {apple banana orange apple}
set sorted_list [lsort -unique $duplicate_list]
puts "Original List: $duplicate_list"
puts "Sorted List (Unique Elements): $sorted_list"
``````

**Output:**
``````
Original List: apple banana orange apple
Sorted List (Unique Elements): apple banana orange
``````

In this example, we sort the list "apple banana orange apple" and remove duplicate elements using the `-unique` option of the `lsort` command. The result is "apple banana orange".
