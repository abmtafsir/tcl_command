## Proc

<details>
<summary>1. Why we use <code>global</code> command inside the procedure?</summary>

**Answer:**

In Tcl, when we declare a variable inside a procedure (proc), it is local to that procedure by default. This means that the variable is only accessible within the scope of the procedure, and any changes made to it will not affect the global variable with the same name, if it exists.

If we want to access or modify a global variable from within a procedure, we need to use the `global` command. The `global` command informs Tcl that a variable is a global variable, making it accessible and modifiable both ***inside and outside the procedure.***

**Here's an example to illustrate the use of `global` inside a proc:**

```tcl
# Declare a global variable
set globalVar 10

# Define a procedure that modifies the global variable
proc modifyGlobalVar {} {
    global globalVar
    set globalVar [expr $globalVar + 5]
    puts "Inside proc: globalVar = $globalVar"
}

# Call the procedure
modifyGlobalVar

# Print the modified global variable outside the procedure
puts "Outside proc: globalVar = $globalVar"
```

In this example, without the `global` command inside the `modifyGlobalVar` procedure, the modification to `globalVar` would create a local variable within the procedure, and it would not affect the global variable outside the procedure. The use of `global` ensures that Tcl knows we are referring to the global variable.

Note that using global variables can make the code harder to understand and maintain. It's generally a good practice to pass variables as arguments to procedures or to use namespaces to encapsulate variables, reducing the reliance on global variables.
</details>


## While Loop

<details>
<summary> Suppose there are numbers from 1-9. If I give any user input except 1 -9, it will give a message and will give another chance untill giving any number from 1 -9. The code is given below </summary>

```tcl
while {1} {
    puts "Enter a number between 1 and 9: "
    flush stdout ; # flush the buffer to make sure the prompt is displayed

    # Read input from the user
    gets stdin user_input

    # Try to convert the input to an integer
    if {[string is integer -strict $user_input]} {
        set number [expr $user_input]

        # Check if the number is in the desired range
        if {$number >= 1 && $number <= 9} {
            puts "You entered a valid number: $number"
            break ; # exit the loop if the input is valid
        } else {
            puts "Invalid input. Please enter a number between 1 and 9. Try again."
        }
    } else {
        puts "Invalid input. Please enter a valid integer between 1 and 9. Try again."
    }
}
```
</details>

## Rabdom

<details>
<summary> 1. Script for time delay</summary>

```tcl
set words {"apple" "banana" "cherry" "date"}

foreach word $words {
    puts $word
    after 1000  ;# Introduce a delay of 1000 milliseconds (1 second)
}
```
</details>

<details>
<summary> 2. Sorting unique value froma  list</summary>

```tcl
#sort the unique elements from a list in ascending order

set myList {4 3 3 2 4 2 3 1 4 1 2 1}
set sortedList [lsort -unique $myList]
puts "Sorted List with Unique Elements: $sortedList"

#sort the unique elements from a list in descending order

set myList {4 3 3 2 4 2 3 1 4 1 2 1}
set sortedList [lsort -unique -decreasing $myList]
puts "Sorted List with Unique Elements: $sortedList"
```
</details>

<details>
<summary> 3. Float to integer</summary>

```tcl
#initialize the value
set num 5.5

#convert from float to int value
set intVal [expr {int($num)}]
puts "Integer value: $intVal" 
```
</details>

<details>
<summary> 4. Split a word into individual alphabets</summary>

```tcl
#Split word into alphabets
set word "hello"
set alphabets [split $word ""]
```
</details>

<details>
<summary> 5. Generate random value </summary>

```tcl
# Define the list of element
set name {Javed Nafi Arnob Mahi Sumaya Rifat Jamil Tafsir Jabin}
puts "The listed names are: $name"

#length of the list
set listLength [llength $name]
#puts "Length of the list is: $listLength"

# generate random index with rand function
set randomIndex [expr (int (rand () * $listLength))]
#puts "Random index: $randomIndex"

# element of the index
set elem [lindex $name $randomIndex]
puts "Name is: $elem"
```
</details>

<details>
<summary> 6. Multi line file context to single line file context</summary>

```tcl
#Version 01:

set fileHandle [open "filename.txt" "r"]
set fileContent [read $fileHandle]
close $fileHandle

set singleLineText [string map {\n " "} $fileContent]
puts $singleLineText

#Version 02:

set fileHandle [open "filename.txt" "r"]
set fileContent [read $fileHandle]
close $fileHandle

regsub -all {\n} $fileContent " " singleLineText
puts $singleLineText
```
</details>

<details>
<summary> 7. Remove punctuation mark</summary>

```tcl
#Version_1:

set text "Hello, World!"
set punctuation {, . ! ?}

# Remove punctuation marks
set cleanText [string map [list {*}$punctuation ""] $text]
puts $cleanText

The string map command replaces each punctuation mark with an empty string, effectively removing them from the original text.


#Version_2:

set text "Hello, World!"
set cleanText [regexp -inline -all -lineanchor {\w+} $text]
puts $cleanText

```
</details>

<details>
<summary> 8. Remove white space and case upper to lower </summary>

```tcl
# define the character in a variable
 set char1 "Listen"
 set char2 "Silent"

# remove whitespace and convert to lowercase
 set word1 [string tolower [string trim $char1]]
 set word2 [string tolower [string trim $char2]]

# remove space from line 
	set sentence "my name is tafsir"
	set sentenceWithoutSpaces [string map {" " ""} $sentence]
	
# split the line into alphabets
set alphabets [split $sentenceWithoutSpaces ""]
```
</details>

<details>
<summary> 9. Sorting string from a list of integer </summary>

```tcl
# define the list_1
set list_1 [list 1 9 7 O 7 22]

# define a null list
set strings {}

# check element is integer with foreach 
foreach element $list_1 {
  if {[string is integer $element]} {
      lappend strings $element
    }   
}

#show the output
puts "The list of integer without string O is :$strings"
```
</details>
