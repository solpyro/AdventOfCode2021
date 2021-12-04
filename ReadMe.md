# Advent of Code 2021

This year I'm attempting the challenges in python using jupyter notebooks

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
Reading the requirements was complicated, and I thought I needed the Gamma and Epsilon values here also. After implementing the filter method to take a flag list, passing in the Gamma or Epsilon flag set, and implementing a recursive filter, I was getting the correct response for the CO2 scrubber value, but a bad value for the O2 generator. 

After reviewing the instructions **again** I realised the majority was recalculated at each filtered version of the report, not from the complete report. This meant copying part of the code I used in my `calculateGamma` method, and I could have refactored the calcultion fo both Gamma and Epsilon to use the new code, but since they won't be used in the future there's not much point.

⭐

## Day 4: ???

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
