A simple python implementation of non-deterministic pushdown automata (PDA).

## Usage

First you need create a automata file where you define your productions, start states and stuff like that.

```python
Q P F # total states
a # input word symbols
Z Y # stack symbols
Q # starting state
Z # starting stack
F # accepting states
F # E - accepts with empty stack or F - accepts with accepting state
Q a Z Q YZ # list of productions (current state, read from word, take from stack, next state, add to stack)
Q a Y Q YY
Q e Z P Z
Q e Y P Y 
P a Z P e 
P a Y P e
P e Z F e
```

When you have a file ready, run the script. It will prompt you for the input file location and then ask for words to test. Enjoy!

> [!NOTE]
> * We agree that "e" means epsilon and will not show up as state symbol.
> * You shouldn't use stack symbols that are longer than one character anything else is fine.

## Issues
This was put together rather quickly, so it would benefit from more edge case tests or tests in general.
