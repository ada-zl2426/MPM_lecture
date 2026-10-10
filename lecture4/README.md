# lecture4

1)  Types of error in python
    -   ImportError: Importing a nonexistent name
    -   ModuleNotFoundError: Module not found
    -   ZeroDivisionError: When dividing by zero
    -   IndexError: Index outside range
    -   TypeError: Unsupported operation for type
    -   SyntaxError: Invalid syntax
    -   IndentationError: Incorrect indentation
    -   RecursionError: Excessive recursive calls

2)  Traceback: When debugging read the traceback error from bottom to top

3)  Static Analysis: To identify issue in code without running
    -   4 static analysis tools
    1)  pyflakes: Detect likely coding mistakes, undefined names, unused imports and some syntax problems
    2)  flake8: Combines Pyflakes, pycodestyle and complexity checks
        -   Pyflakes: code mistakes
        -   pycodestyle: code style
        -   Complexity
    3)  pylint: More comprehensive and opinionated code checking
        -   More extensive checks
            -   Unused variables and imports.
            -   Undefined names.
            -   Various suspicious coding patterns.
            -   Naming and style issues.
            -   Potential design problems.
    4)  ruff: Extremely fast analyser that supports Flake8-style checks and many additional rules  
        -   It implements Flake8-style checks and many additional rules

4)  Understanding flake8 output
    Example:
    example.py:4:14: F821 undefined name 'z'
    example.py	Filename
    4 -> Line number
    14 -> Column number
    F821 -> Diagnostic code
    undefined name 'z' -> Description of the issue

    Diagnostic code starting letter
    F -> Pyflakes: Potential coding mistakes or unnecessary code
    E -> pycodestyle: Style errors
    W -> pycodestyle: Style warnings

5)  Runtime debugging: Run the program, encounter an error and start investigating

6)  Minimum failing example:    The minimal amount of code that can be used to replicate the bug

7)  Manual debugging
    -   print(): display variable values as code runs
    -   breakpoint():   Pause the program and inspect it interactively
    -   from IPython import embed; embed(): Open an interactive python session in a running script
  
