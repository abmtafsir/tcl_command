# lsearch

## Introduction:

The `lsearch` command in Tcl is used to search for elements in a list. It allows us to find the index of a specific element, count occurrences, or check if an element exists in the list. The `lsearch` command uses a pattern to perform the search. 

## Syntax:

`lsearch ?-exact? ?-regexp? ?-all? ?-inline? ?--? list pattern`


- `-exact`: Performs an exact match search. It is the default behavior if neither `-exact` nor `-regexp` is provided.
- `-regexp`: Performs a regular expression match search.
- `-all`: Returns all matching indices or elements instead of just the first one.
- `-inline`: Returns the elements themselves instead of their indices.
- `--`: Indicates the end of options to avoid ambiguity if the `pattern` starts with `-`.

## Examples and Explanations:

### Example 1: Exact Match Search

**Code:**
``````
set my_list {apple banana orange}
set index [lsearch $my_list "banana"]
puts "Index of 'banana': $index"
``````

**Output:**
``````
Index of 'banana': 1
``````
In this example, we have a list "apple banana orange" and we use the `lsearch` command with the pattern "banana" to perform an exact match search. The index of the first occurrence of "banana" in the list is obtained, which is 1.

### Example 2: Regular Expression Match Search

**Code:**
``````
set my_list {apple banana orange}
set indices [lsearch -regexp $my_list "a.*"]
puts "Indices of elements starting with 'a': $indices"
``````

**Output:**
``````
Indices of elements starting with 'a': 0 
``````

In this example, we have a list "apple banana orange" and we use the `lsearch` command with the `-regexp` option and the pattern "a.*" to perform a regular expression match search. This pattern matches elements that start with the letter 'a'. The indices of all matching elements are obtained.

### Example 3: Exact Match Count (VVI)

**Code:**
``````
set my_list {apple banana orange apple}
set count [lsearch -all $my_list -exact "apple"]
puts "Count of 'apple': $count"
``````

**Output:**
``````
Count of 'apple': 2
``````

In this example, we have a list "apple banana orange apple" and we use the `lsearch` command with the `-all` option and the pattern "apple" to count all exact matches of "apple" in the list. The count of occurrences is obtained, which is 2.

### Example 4: Inline Search

**Code:**
``````
set my_list {apple banana orange}
set matches [lsearch -inline $my_list "banana"]
puts "Matches: $matches"
``````

**Output:**
``````
Matches: banana
``````

In this example, we have a list "apple banana orange" and we use the `lsearch` command with the `-inline` option and the pattern "banana" to obtain the actual matching element. The element "banana" itself is obtained.

### Example 5: Element Existence Check

**Code:**
``````
set my_list {apple banana orange}
if {[lsearch -exact $my_list "apple"] >= 0} {
    puts "Element 'apple' exists in the list."
} else {
    puts "Element 'apple' does not exist in the list."
}
``````

**Output:**
``````
Element 'apple' exists in the list.
``````

In this example, we have a list "apple banana orange" and we use the `lsearch` command with the `-exact` option and the pattern "apple" to check if the element "apple" exists in the list. Since the return value is greater than or equal to 0, it indicates that the element exists in the list.

