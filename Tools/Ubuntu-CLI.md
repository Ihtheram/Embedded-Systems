# Ubuntu Command Line Interface

#### **[⇐ Embedded Engineering Tools](../Embedded-Engineering-Tools.md)**
---

## Basic Commands

* `pwd` : View present working directory
* `ls` : View a list of sub-directories and files
* `./<filename>`: Run a file at current directory
* `cd` : Change to the outer directory
* `cd <path>` : Change to the directory at the specified path
* `cat > <filename>.<extension>` : Create a text file with a specified name and a specified extension and insert text on the next line


### Refresh Local Package Index

`sudo apt update`

## GNU
* Install Essential Building Tools

    `sudo apt install build-essential`
        
    installs gcc, g++, make, and other tools needed for compiling C/C++ code.

* Install GCC Only

    `sudo apt install gcc`

    Requires [refreshing local package index](#refresh-local-package-index)


## VIM
* `vim <filename>{.<extension>}` : opens specified file in vim.
* `i`: from normal to editing mode
* `esc`: from editing to normal mode
* `:w` : save changes
* `shift + ZZ` : save and quit vim
* `shift + ZQ` : quit vim without saving

## GCC
* Compile / build the `.c` file and generate a `.out` binary file with the specified name

    `gcc -o <binaryfile>.out <file>.c`

* Run the compiled / built file

    `./<binaryfile>.out`