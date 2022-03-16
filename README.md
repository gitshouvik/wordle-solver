# wordle-solver
## A Mathematica code to solve Wordle. 


The syntax to use the code is

```
wordle["lettersToKeep","lettersToRemove",{list_of_correct_letter_positions},{list_of_wrong_positions}]
```

### Example

If we know that \
(a) the word contains "s", "l" and "p", \
(b) does not contain "o", "e", "c" and "a", \
(c) "s" is located at position 1 and "l" is located at position 4, and \
(d) "p" is not located at position 5, \
the corresponding code is 

```
wordle["slp", "oeca", {{"s", 1}, {"l", 4}}, {{"p", 5}}]
```
This then gives the output
```
{"scalp", "slaps", "slips", "slump", "slurp", "spill", "splat", "splay", "split", "sylph"}
```
We can enter any of the words above next on Wordle. If we enter "SCALP" and if Wordle tells us \
(a) "c" and "a" are absent, \
(b) "s" is at position 1 and "l" is at position 4, and \
(c) "p" is not at position 5,
we modify the above code to:
```
wordle["slp", "oeca", {{"s", 1}, {"l", 4}}, {{"p", 5}}]
```
and the output to this is
```
{"spill"}
```
This is one lucky situation where the word is unique. However, performing three or four iterations like the above gives a fairly short list of words to guess the word correctly. There is still some element of luck and some amount of mental expenditure involved in the process. 
