# wordle-solver
## A Mathematica code to solve Wordle. 


The syntax to use the code is

```
wordle["lettersToKeep","lettersToRemove",{list_of_correct_letter_positions},{list_of_wrong_positions}]
```

To download the Mathematica file click the "Code" button above and then "Download ZIP". 

### Example

Let's say we enter "SLOPE" in Wordle and it tells us that:
(a) the word contains "s", "l" and "p", \
(b) does not contain "o" and "e", \
(c) "s" is located at position 1, and \
(d) "l" is not at position 2 and "p" is not located at position 4, \
the corresponding code is 

```
wordle["slp", "oe", {{"s", 1}}, {{"l", 2}, {"p", 4}}]
```
This then gives the output
```
{"scalp", "spill", "splat", "splay", "split"}
```
We can enter any of the words above next on Wordle. If we enter "SCALP" and if Wordle tells us \
(a) "c" and "a" are absent, \
(b) "s" is at position 1 and "l" is at position 4, and \
(c) "p" is not at position 5, \
we modify the above code to:
```
wordle["slp", "oeca", {{"s", 1}, {"l", 4}}, {{"p", 5}}]
```
and the output to this is
```
{"spill"}
```
This is one lucky situation where the word is unique. However, performing three or four iterations like the above gives a fairly short list of words to guess the word correctly. There is still some element of luck and some amount of mental expenditure involved in the process. 
