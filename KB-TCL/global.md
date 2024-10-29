# global

## Introduction:

In Tcl, the global command is used to declare global variables within a procedure. This allows you to create or modify variables that are outside the scope of the current procedure, making them accessible throughout the script.

## Example:


**Code:**
``````
proc myProcedure {} {
    global myVariable
    set myVariable "Hello, World!"
}

# Call the procedure
myProcedure

# Access the global variable
puts $myVariable
``````

**Output:**
``````
Hello,World!"
``````
**In this example:**

1. We define a procedure called myProcedure that uses the global command to declare the global variable myVariable.
2. Inside the procedure, we set the value of myVariable to "Hello, World!"
3. After calling the procedure, we can access myVariable from anywhere in the script, not just within the procedure's scope.
