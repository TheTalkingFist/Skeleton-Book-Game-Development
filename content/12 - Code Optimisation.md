Legend:

<font color="#0070c0">tldr</font>

<font color="#00b050">Useful to Remember/Examples</font>

<font color="#ff0000">A Must to Memorize </font>

## Agenda

- #WhatIsIt
- #Advantages
- #TypesOfOptimisations

## What is Code Optimisation?

It is the code modification to improve code quality and efficiency.

This is so that optimised code becomes smaller in size, consumes less memory, and executes more rapidly. But It is Important that Before and After optimised code should produce the same outcome.


## Advantages

- Faster Execution Speed
- Memory Efficient
- Better Performance

## Code Optimisation Techniques

- **Compile Time Evaluation**
    - Constant Folding
    - Constant Propagation

- **Common Subexpression Elimination**
    - Forward Subexpression Elimination
    - Backwards Subexpression Elimination

- **Code Motion**
    - Instruction Reordering
    - Global Code Motion

- **Strength Reduction**
    - Multiplication to +/-
    - Bitwise Operations


### Compile Time Evaluation

#### Constant Folding

Simplifies Expressions at compile time by replacing it with their computed constant values.

This results in only needing constants the can be determined ahead of time which eliminated the need for runtime computations

**Advantages:**
- Improved runtime performance
- Reduced runtime memory usage
- Code Size Reduction
- Simplified Code Logic


Operands having constant values are evaluated at the compile time


<font color="#0070c0">TLDR: </font>
You Pre-Calculate instead of the computer doing it when the game is running.


#### Constant Propagation

Replaces variables with their known constant values throughout the program.

This eliminates unnecessary variable assignments and calculations by propagating constant values through code.

**Advantages:**

- Reduces Variable Lookups 
- Eliminates Unnecessary computations
- Code Size Reduction
- Improved code readability

Constants assigned to a variable can be substituted at the use of the variable.

<font color="#0070c0">TLDR:</font>
Instead of deriving what's in the variables, just put the value other there.



### Common Subexpression Elimination

This aims to eliminate redundant computations by identifying and reusing the common subexpressions, reducing the number of repeated calculations.


### Code Motion

Moves code instructions or computations to new locations within the program.

This reduces the evaluation frequency of expression, and improves the performance by reducing redundant computations and minimising memory access.


### Strength Reduction

Replaces "Expensive" Operations with cheaper or more efficient alternatives.

Reducing Complexity of the code by simplifying or optimising certain operations.


## Types of Optimisation

### Machine independent optimisation

Improves code and efficiency across different hardware architectures and platforms, eliminating inefficiencies and maximizing code portability.

This ensures the code performs very well on a variety of machines without relying on specific hardware optimisations or features.


### Machine Dependant Optimisation

Optimising code for a particular platform or hardware architecture.

taking into consideration unique capabilities of the target hardware, and may not be portable across different machines.


### Code Refactoring

The process of restructuring and improving existing code without changing its external behaviour, 

Simplifying complex code and eliminate redundant or duplicate code.

This would involve making changes to:
     -  Improve code's internal structure
     - Improve design
     - improve maintainability
     - improve performance
     - improve code readability

#### Code Refactoring Techniques

##### Extract Method

Involves taking a Portion of code from within a larger method and moving it into a separate, self-contained method.

Extraction Breaks down the code into smaller chunks  that performs a specific task, said chunk is then extracted into a new method  and the original code is replaced with a method call to the newly created method.

##### Inline Method

Involves replacing a method call with the actual code from the method itself

Inline refactoring is used when a method is no longer necessary or provides little value, so we can simplify  by directly inserting its code into the calling location.

By finding all calls to the method and replacing them with the content of the method, the method can then be deleted

A Reverse of the Extract Method