# string map

## Introduction 

The `string map` command in Tcl is used to perform multiple string replacements in a single operation. It allows you to replace specified substrings with corresponding replacement strings within a given input string.


## Syntax

The syntax of the `string map` command is as follows:

`string map {mapping} string`


- `mapping`: A list of pairs where each pair consists of a substring to be replaced and its corresponding replacement substring. Multiple pairs are enclosed in curly braces `{}` and separated by spaces.
- `string`: The input string in which the replacements should be performed.


## Examples and Explanations

### Example 1: Simple String Replacement

**Code:**
``````
set sentence "Hello, World!"
set modifiedSentence [string map {"Hello" "Hi"} $sentence]

puts "Original String: '$sentence'"
puts "Modified String: '$modifiedSentence'"
``````

**Output:**
``````
Original String: 'Hello, World!'
Modified String: 'Hi, World!'
``````

In this example, the `sentence` variable contains the input string `Hello, World!`. The `string map` command is used to replace the substring `Hello` with `Hi`. The resulting modified string is stored in the `modifiedSentence` variable.


### Example 2: Multiple String Replacements

**Code:**
``````
set sentence "The quick brown fox jumps over the lazy dog."
set modifiedSentence [string map {"quick" "fast" "brown" "red"} $sentence]

puts "Original String: '$sentence'"
puts "Modified String: '$modifiedSentence'"
``````

**Output:**
``````
Original String: 'The quick brown fox jumps over the lazy dog.'
Modified String: 'The fast red fox jumps over the lazy dog.'
``````

In this example, the `sentence` variable contains the input string `The quick brown fox jumps over the lazy dog.` The `string map` command is used to perform multiple replacements. The substring `quick` is replaced with `fast`, and the substring `brown` is replaced with `red`. The resulting modified string is stored in the `modifiedSentence` variable.


### Example 3: Case-Insensitive Replacements

**Code:**
``````
set sentence "Hello, hello, HELLO!"
set modifiedSentence [string map -nocase {"hello" "Hi"} $sentence]

puts "Original String: '$sentence'"
puts "Modified String: '$modifiedSentence'"
``````

**Output:**
``````
Original String: 'Hello, hello, HELLO!'
Modified String: 'Hi, Hi, Hi!'
``````

In this example, the `sentence` variable contains the input string `Hello, hello, HELLO!`. The `-nocase` option is used with the `string map` command to perform case-insensitive replacements. The substring "hello" is replaced with `Hi` regardless of its case. The resulting modified string is stored in the `modifiedSentence` variable.


### Example 4: Remove Space Between Characters

**Code:**
``````
set sentence "Hello,    World!"
set modifiedSentence [string map {" " ""} $sentence]

puts "Original String: '$sentence'"
puts "Modified String: '$modifiedSentence'"
``````

**Output:**
``````
Original String: 'Hello,    World!'
Modified String: 'Hello,World!'
``````

In this example, the `sentence` variable contains the input string `Hello,    World!` with multiple spaces between "Hello," and "World!". The `string map` command is used to replace the space character `" "` with an empty string `""`. As a result, all spaces are removed from the string, producing the modified string `Hello,World!`.


### Example 5: Replace the Character from a List

**Code:**

``````
# initialize a sentence

set sentence "Hello, world! How are you?"
puts "sentence: $sentence"

# initialize a list to replace

set replace {"Hello" "Hi"}

# replace the content of the list with a string map

foreach {original duplicate} $replace {
set replace [string map [list $original $duplicate] $sentence]
  }
puts "replace: $replace"
``````
**Output:**
``
sentence: Hello, world! How are you?
replace: Hi, world! How are you?
``````

### Example 6: Remove White Space Within a String


**Code:**
``````
set sentence "Hello,     World!"
set trimmedSentence [string trim [string map {" " ""} $sentence]]

puts "Original String: '$sentence'"
puts "Trimmed String: '$trimmedSentence'"
``````
**Output:**
``````
Original String: 'Hello,     World!'
Trimmed String: 'Hello,World!'
``````
In this example the sentence `Hello,  World` is stored in the sentence variable. The `string map` cut off the space in between `Hello,` and `World!` and stored in `trimmedSentence`


