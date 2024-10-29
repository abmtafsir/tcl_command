# file handling

## Introduction:

File handling in Tcl is a fundamental aspect of working with files and data. Tcl provides simple and powerful mechanisms for reading from and writing to files. Here are the basic file-handling operations in Tcl, including opening, reading, writing, and closing files.

**1. Opening a File**

We can use the `open` command to open a file. It returns a file handle that we can use for subsequent operations on the file.

**Code:**

```
    set fileHandle [open "filename.txt" mode]
```


- `"filename.txt"` is the name of the file we want to open.
- `mode` specifies the mode for opening the file, which can be one of the following:
	- `r`: Opens an existing text file for reading purposes and the file must exist. This is the default mode used when no access mode is specified.
    - `w`: Opens a text file for writing, if it does not exist, then a new file is created else the existing file is truncated.
	- `a`: Opens a text file for writing in appending mode and the file must exist. Here, our program will start appending content in the existing file content.
	- `r+`:Opens a text file for reading and writing both. The file must exist already.
	-`w+`: Opens a text file for reading and writing both. It first truncates the file to zero length if it exists otherwise create the file if it does not exist.
	- `a+`: Opens a text file for reading and writing both. It creates the file if it does not exist. The reading will start from the beginning, but writing can only be appended.

**2. Reading from a File**

To read from a file, you can use the `gets` command to read one line at a time, or you can use the `read` command to read a specific number of bytes.

Using `gets`:

**Code:**

``````
set fileHandle [open "filename.txt" r]
while {[gets $fileHandle line] >= 0} {
    # Process each line
    puts $line
}
close $fileHandle
``````
**Explanation:**

- The gets function returns -1 when it reaches the end of the file or encounters an error (e.g., if the file doesn't exist).
- It returns 0 if it successfully reads a line from the file.
- In the code, the condition `while {[gets $fileHandle line]>=0}`  uses the `gets` function to read lines from the file "filename.txl" and processes them one by one. The condition `>=0` in this context is used to check if the `gets` function successfully reads a line from the file.

**Using `read`:**

**Code:**

``````
set fileHandle [open "filename.txt" r]
set content [read $fileHandle]
puts "The contents of the fileHandle is $content"
close $fileHandle
``````

**3. Writing to a File**

To write data to a file, we can use the `puts` or `write` command.

**Using `puts`:**

**Code:**

``````
set fileHandle [open "filename.txt" w]
puts $fileHandle "Hello, World!"
close $fileHandle
``````

**Using `write`:**

**Code:**

``````
set fileHandle [open "filename.txt" w]
set data "Hello, World!"
write $fileHandle $data
close $fileHandle
``````

**4. Appending to a File**

To append data to an existing file, we can open the file in append mode (`a`).

**Code:**

``````
set fileHandle [open "filename.txt" a]
puts $fileHandle "This line will be appended."
close $fileHandle
``````

**5. Closing a File**

Always close a file when you are done with it using the `close` command. This ensures that any changes are saved, and system resources are released.

**Code:**
``````
set fileHandle [open "filename.txt" r]
# Perform read or write operations
close $fileHandle
``````

**6. Checking for File Existence**

You can use the `file exists` command to check if a file exists before attempting to open or manipulate it.

**Code:**

``````
if {[file exists "filename.txt"]} {
    set fileHandle [open "filename.txt" r]
    # Perform file operations
    close $fileHandle
} else {
    puts "File does not exist."
}
``````

**7. Error Handling**

Always include error handling in your file operations. Check for errors when opening, reading, or writing to files to ensure your script gracefully handles unexpected situations.

**Code:**

``````
set fileHandle [open "filename.txt" "r"]
if {[catch {gets $fileHandle line} errorMsg]} {
    puts "Error: $errorMsg"
} else {
    # Process the line
}
close $fileHandle
``````

**Example: Write a TCL Scripting for Markdown formatting.**

``````
Code:
#Task: Write a TCL Scripting for Markdown formatting.
#Algorithms:
#   1. make a file that already exists containing the questions named "question.md"
#   2. open "question.md" in read mode 
#   3. open "filename.md" in read and write mode 
#   4. enter the "filename.md" and write the markdown format 
##################################################################################

#open file "question.md" in read mode which already exists in the current location
set file_read [open "questions.md" r]
#open "filename.md" in read and write mode and change the "filename.md" according to the corresponding file
set file_read_write [open "filename.md" w+] 


# while loop read each line one by one from "file_read" till the end of the file using gets command
# the contents of each line stored in the "question" variable 
# at the end of the line the condition becomes false because gets function returns -1 which is not >= 0.

while {[gets $file_read question]>=0} {
    puts $file_read_write "<details>\n<summary>$question</summary>\n\n**<u>Short Answer:</u>**\n\n**<u>Detailed Answer:</u>**\n\n**<u>Example:</u>**</details>\n"
}
close $file_read_write
close $file_read
``````
