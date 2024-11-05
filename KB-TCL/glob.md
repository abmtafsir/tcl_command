# glob

## Introduction

In Tcl (Tool Command Language), `glob` is a command used to perform file name pattern matching, which is commonly referred to as "globbing". It allows you to match files and directories based on wildcard patterns, similar to how globbing works in Unix shells. The `glob` command is an essential tool when you need to list files or directories that match a certain pattern, such as all `.txt` files or all files beginning with "data".

---

### 1. **Syntax of `glob`**

The basic syntax of the `glob` command is:

```tcl
glob ?switches? pattern
```

- **pattern**: A pattern string that contains wildcards (like `*`, `?`, or `[]`) to match file names.
- **switches**: Optional flags that modify the behavior of `glob`. For instance, you can use `-directory` to specify a particular directory to search in.

### 2. **Wildcards in `glob` patterns**

The glob command uses several special wildcard characters to match file names:

- `*` (asterisk): Matches any string of characters (including an empty string).
- `?` (question mark): Matches exactly one character.
- `[...]` (brackets): Matches any one of the characters enclosed in the brackets. For example, `[a-c]` matches 'a', 'b', or 'c'.
- `{...}` (brace expansion): Matches one of the alternatives separated by commas. For example, `{a,b,c}` will match 'a', 'b', or 'c'.

### 3. **Basic Examples**

#### 3.1. Simple File Matching

To match all files in the current directory:

```tcl
glob *
```

This will return a list of all files and directories in the current working directory.

#### 3.2. Match Files with Specific Extensions

To find all `.txt` files in the current directory:

```tcl
glob *.txt
```

This will return a list of all files ending in `.txt`.

#### 3.3. Using `?` for Single Character Matching

To find all files with a single character before `.txt`:

```tcl
glob ??.txt
```

This will return all files like `ab.txt`, `12.txt`, but not `a.txt` or `abc.txt`.

#### 3.4. Using Brackets for Character Sets

To match all `.txt` files that start with either "a" or "b":

```tcl
glob [ab]*.txt
```

This will return `apple.txt`, `banana.txt`, etc., but not `cat.txt`.

#### 3.5. Using Braces for Alternative Patterns

To match files with either `.txt` or `.log` extensions:

```tcl
glob *.{txt,log}
```

This will return files that end in either `.txt` or `.log`.

---

### 4. **Advanced Usage of `glob`**

#### 4.1. Specifying a Directory

By default, `glob` will search in the current working directory. If you want to search in a specific directory, you can specify the directory as part of the pattern:

```tcl
glob /path/to/directory/*.txt
```

This will return all `.txt` files in the specified directory.

#### 4.2. Recursive Search with `glob` and `**`

Tcl 8.6 and later supports recursive globbing with the `**` pattern. This allows you to search for files in all subdirectories:

```tcl
glob **/*.txt
```

This will return all `.txt` files in the current directory and all of its subdirectories.

#### 4.3. Filtering with `-types` (Unix-Style Switch)

In Unix-like operating systems, `glob` can be used with `-types` to filter files by type. For instance, you can match only directories or only regular files:

```tcl
glob -types f *.txt   ;# Match only regular files
glob -types d */      ;# Match only directories
```

Note: This option is platform-dependent and may not be available in all Tcl installations.

---

### 5. **Return Values**

The `glob` command returns a list of files that match the pattern. The result is always a list, even if only one file matches. If no files match, it returns an empty list.

Example:

```tcl
set files [glob *.txt]
if {[llength $files] == 0} {
    puts "No .txt files found!"
} else {
    puts "Found .txt files: $files"
}
```

This will check if there are any `.txt` files in the current directory and print a message based on whether any files match.





