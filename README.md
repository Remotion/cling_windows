Cling - The Interactive C++ Interpreter
=========================================

[Cling](https://github.com/root-project/cling).exe build for Windows.

Overview
--------
Cling is an interactive C++ interpreter, built on top of Clang and LLVM compiler
infrastructure. Cling realizes the [read-eval-print loop
(REPL)](http://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)
concept, in order to leverage rapid application development. Implemented as a
small extension to LLVM and Clang, the interpreter reuses their strengths such
as the praised concise and expressive compiler diagnostics.

See also [cling's web page.](https://cdn.rawgit.com/root-project/cling/master/www/index.html)

Usage
--------
```
Cling (C/C++ interpreter) meta commands usage
All commands must be preceded by a '.', except
for the evaluation statement { }

Syntax: .Command [arg0 arg1 ... argN]

   .L <filename>                - Load the given file or library

   .(x|X) <filename>[args]      - Same as .L and runs a function with
                                  signature: ret_type filename(args)

   .> <filename>                - Redirect command to a given file
      '>' or '1>'               - Redirects the stdout stream only
      '2>'                      - Redirects the stderr stream only
      '&>' (or '2>&1')          - Redirects both stdout and stderr
      '>>'                      - Appends to the given file

   .undo [n]                    - Unloads the last 'n' inputs lines

   .U <filename>                - Unloads the given file

   .I [path]                    - Shows the include path. If a path is given -
                                  adds the path to the include paths

   .O <level>                   - Sets the optimization level (0-3)
                                  (not yet implemented)

   .class <name>                - Prints out class <name> in a CINT-like style

   .files                       - Prints out some CINT-like file statistics

   .fileEx                      - Prints out some file statistics

   .g                           - Prints out information about global variable
                                  'name' - if no name is given, print them all

   .@                           - Cancels and ignores the multiline input

   .rawInput [0|1]              - Toggle wrapping and printing the
                                  execution results of the input

   .dynamicExtensions [0|1]     - Toggles the use of the dynamic scopes and the
                                  late binding

   .printDebug [0|1]            - Toggles the printing of input's corresponding
                                  state changes

   .storeState <filename>       - Store the interpreter's state to a given file

   .compareState <filename>     - Compare the interpreter's state with the one
                                  saved in a given file

   .stats [name]                - Show stats for internal data structures
                                  'ast'  abstract syntax tree stats
                                  'asttree [filter]'  abstract syntax tree layout
                                  'decl' dump ast declarations
                                  'undo' show undo stack

   .help                        - Shows this information

   .q                           - Exit the program
```
