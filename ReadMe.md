# Advent of Code 2021

This year I'm attempting the challenges in python 3 using jupyter notebooks. This feels kind of limiting, but lets see how far I get before I switch to something else... or give up.

## Day 1: Sonar Sweep

Nothing too special here, just a for loop and a simple comparison.

My sliding frame implementation is very lazy :D

⭐⭐

## Day 2: Dive!

I thought it would be nicer to read the puzzle data directly from the url, but I dont know how to do that authentication in python's urllib, so I'll leave that and just get on with the puzzle.

Again nothing too special in my code here, but it's nice to be able to use tuples.

⭐⭐

## Day 3: Binary Diagnostic

# Calculate Power Consumption

Lots of simple lsits and parsing characters in strings. At least calculating the Epsilon value was easy once the Gamma was calculated. I'd hoped to get Gamma as an int and use ~ to calculate Epsilon for free, but python uses 16-bit ints so the value would have been off.

⭐

# Verify Life Support Rating

Reading the requirements was complicated, and I thought I needed the Gamma and Epsilon values here also. After implementing the filter method to take a flag list, passing in the Gamma or Epsilon flag 
set, and implementing a recursive filter, I was getting the correct response for the CO<sub>2</sub> scrubber value, but a bad value for the O<sub>2</sub> generator. 

After reviewing the instructions **again** I realised the majority was recalculated at each filtered version of the report, not from the complete report. This meant copying part of the code I used in my `calculateGamma` method, and I could have refactored the calcultion fo both Gamma and Epsilon to use the new code, but since they won't be used in the future there's not much point.

⭐

## Day 4: Giant Squid

It took some work just to parse the input data! Running the bingo game also looked daunting, but breaking the tasks down enough made most of them easy enough. The tricky part was recognising a winning board.

After looking through other solutions, I decidered there's no clever maths underneath this puzzle, so I'm solveing it in a bruteforcy way; running the solution to part 1 in a while loop, and removing the first winner from the list of boards as we go.

⭐⭐

## Day 5: ???

## Day 6: ???

## Day 7: ???

## Day 8: ???

## Day 9: ???

## Day 10: ???

## Day 11: ???

## Day 12: ???

## Day 13: ???

## Day 14: ???

## Day 15: ???

## Day 16: ???

## Day 17: ???

## Day 18: ???

## Day 19: ???

## Day 20: ???

## Day 21: ???

## Day 22: ???

## Day 23: ???

## Day 24: ???

## Day 25: ???
