# Architecture and Technologies

This is where we discuss the software architecture and techologies we'll be using for this project.

## Technologies

* Node.js - I like working with it and it's what I'm learning to use
* Lodash - Contains all sorts of useful functionality
* Immutable.js - Immutable data structures for functional programming
* Jest - Used for unit testing
* Chalk - Used for styled terminal output
* Clear - Used for clearing the terminal
* Inquirer or Vorpal - Command prompt functionality
* Blessed and Blessed-contrib - Really fancy terminal functionality (won't be used initially, but may be in the future)

## Software Architecture

I haven't worked with any functional languages yet, but I'm going to make the code as functional as possible given my skill level with functional code. It will likely end up being a bit of a mix between imperative and functional code.

Immutable.js will be used for data structures. Data will not be mutated, but immutable data should always be used.

Functions with side effects should be cleanly separated from functions with side effects (typically any sort of I/O). This should enable easier unit testing.

Any sort of UI code (even the code without side effects) should be separated from game logic code.

Ideas:

- Generate the current menu from the game state
- Hand the current menu off to another function for output
- Generate the game board from the game state
- Hand the game board off to another function for output
- Input code should convert the characters to commands and hand the command off to another function for processing
- Command processing function should return some sort of code, which is passed to another function for output handling