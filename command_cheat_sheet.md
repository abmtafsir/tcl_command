Tcl (Tool Command Language) is a scripting language that is known for its simplicity and extensibility. Below is a list of some common Tcl commands grouped by functionality. Note that Tcl is extensible, and you can define your own commands as well.

### Basic Commands

1. `set` - Assigns a value to a variable.
   ```tcl
   set var_name value
   ```

2. `puts` - Prints to the console or to a file.
   ```tcl
   puts "Hello, World!"
   ```

3. `expr` - Evaluates an expression.
   ```tcl
   expr {1 + 2}
   ```

4. `if` - Conditional statement.
   ```tcl
   if {condition} {
       # commands
   } else {
       # commands
   }
   ```

5. `while` - A loop with a condition.
   ```tcl
   while {condition} {
       # commands
   }
   ```

6. `for` - A C-style loop.
   ```tcl
   for {set i 0} {$i < 10} {incr i} {
       # commands
   }
   ```

7. `foreach` - Loop over a list of values.
   ```tcl
   foreach var {list_of_values} {
       # commands
   }
   ```

8. `incr` - Increment a variable.
   ```tcl
   incr var_name
   ```

9. `proc` - Defines a procedure (function).
   ```tcl
   proc name {args} {
       # commands
   }
   ```

10. `return` - Returns a value from a procedure.
    ```tcl
    return value
    ```

11. `break` - Exits a loop.
    ```tcl
    break
    ```

12. `continue` - Skips the rest of the loop body.
    ```tcl
    continue
    ```

### File and I/O Commands

1. `open` - Opens a file for reading or writing.
   ```tcl
   set file [open "filename.txt" r]
   ```

2. `close` - Closes an open file.
   ```tcl
   close $file
   ```

3. `read` - Reads from an open file.
   ```tcl
   set data [read $file]
   ```

4. `gets` - Reads a line from a file.
   ```tcl
   gets $file line
   ```

5. `puts` - Writes a string to a file.
   ```tcl
   puts $file "Hello, World!"
   ```

### String Manipulation

1. `string length` - Get the length of a string.
   ```tcl
   string length "hello"
   ```

2. `string compare` - Compare two strings.
   ```tcl
   string compare "abc" "def"
   ```

3. `string trim` - Trim whitespace.
   ```tcl
   string trim "  hello  "
   ```

4. `string index` - Get the character at a specified index.
   ```tcl
   string index "hello" 1
   ```

5. `string match` - Check if a string matches a pattern.
   ```tcl
   string match "*world" "hello world"
   ```

### List Commands

1. `list` - Create a list.
   ```tcl
   set mylist [list 1 2 3]
   ```

2. `lindex` - Get an element from a list by index.
   ```tcl
   lindex $mylist 0
   ```

3. `llength` - Get the length of a list.
   ```tcl
   llength $mylist
   ```

4. `lappend` - Append to a list.
   ```tcl
   lappend mylist 4
   ```

5. `linsert` - Insert elements into a list.
   ```tcl
   linsert $mylist 1 99
   ```

6. `lsearch` - Search for an element in a list.
   ```tcl
   lsearch $mylist 2
   ```

7. `lsort` - Sort a list.
   ```tcl
   lsort $mylist
   ```

### Control Flow

1. `switch` - Case-based branching.
   ```tcl
   switch $var {
       1 { puts "one" }
       2 { puts "two" }
       default { puts "other" }
   }
   ```

2. `catch` - Catch errors and exceptions.
   ```tcl
   catch {code} result
   ```

### Dictionary Commands (Tcl 8.5+)

1. `dict create` - Create a dictionary.
   ```tcl
   dict create key1 value1 key2 value2
   ```

2. `dict set` - Set a key-value pair.
   ```tcl
   dict set mydict key value
   ```

3. `dict get` - Retrieve a value by key.
   ```tcl
   dict get mydict key
   ```

4. `dict exists` - Check if a key exists.
   ```tcl
   dict exists mydict key
   ```

### Miscellaneous Commands

1. `eval` - Evaluate a command.
   ```tcl
   eval {puts "hello"}
   ```

2. `exec` - Execute a system command.
   ```tcl
   exec ls
   ```

3. `after` - Schedule a command after a delay.
   ```tcl
   after 1000 {puts "1 second later"}
   ```

4. `time` - Measure the time a command takes.
   ```tcl
   time {expr 1+2}
   ```

5. `exit` - Exit the interpreter.
   ```tcl
   exit
   ```

