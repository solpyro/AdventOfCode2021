# Advent of Code 2021

This year I'm attempting the challenges in python 3 using jupyter notebooks. This feels kind of limiting, but lets see how far I get before I switch to something else... or give up.

## Day 1: Sonar Sweep ⭐⭐

Nothing too special here, just a for loop and a simple comparison.

My sliding frame implementation is very lazy :D

### Techniques leared

General refresher of python syntax (it's been a while)

## Day 2: Dive! ⭐⭐

I thought it would be nicer to read the puzzle data directly from the url, but I dont know how to do that authentication in python's urllib, so I'll leave that and just get on with the puzzle.

Again nothing too special in my code here, but it's nice to be able to use tuples.

## Day 3: Binary Diagnostic ⭐⭐

### Calculate Power Consumption

Lots of simple lsits and parsing characters in strings. At least calculating the Epsilon value was easy once the Gamma was calculated. I'd hoped to get Gamma as an int and use ~ to calculate Epsilon for free, but python uses 16-bit ints so the value would have been off.

### Verify Life Support Rating

Reading the requirements was complicated, and I thought I needed the Gamma and Epsilon values here also. After implementing the filter method to take a flag list, passing in the Gamma or Epsilon flag 
set, and implementing a recursive filter, I was getting the correct response for the CO<sub>2</sub> scrubber value, but a bad value for the O<sub>2</sub> generator. 

After reviewing the instructions **again** I realised the majority was recalculated at each filtered version of the report, not from the complete report. This meant copying part of the code I used in my `calculateGamma` method, and I could have refactored the calcultion fo both Gamma and Epsilon to use the new code, but since they won't be used in the future there's not much point.

### Techniques leared

- Ternary statments: `('trueValue' if isTrue else 'falseValue')`  
- List filtering: `[element for element in list if isTrue]`
- Enumerate list: `for i,v in enumerate(list)`

## Day 4: Giant Squid ⭐⭐

It took some work just to parse the input data! Running the bingo game also looked daunting, but breaking the tasks down enough made most of them easy enough. The tricky part was recognising a winning board.

After looking through other solutions, I decidered there's no clever maths underneath this puzzle, so I'm solveing it in a bruteforcy way; running the solution to part 1 in a while loop, and removing the first winner from the list of boards as we go.

### Techniques leared

- List mapping: `[function(element) for element in list]`
- Initilizing empty lists: `list = [defaultValue]*length`
- Iterate of part of a list: `for element in list[start:end]`
- The difference & similarities between lists `[]` and dictionaries `{}`

## Day 5: Hydrothermal Venture ⭐⭐

Some basic assumptions made part 1 trickier than it should have been. Firstly, I hoped that I could just implement drawing lines in all directions, and filter the coordinates to just the straight lines, but I soon realized that the logic for drawing diagonal lines was more complicated (and probably specified in part 2).  
My second mistake was just passing x1 and x2 into the `range` function. Since some of the lines go backwards, they weren't being drawn, and were giving me bad results. in the end I defined my range as `range(min(x1,x2),max(x1,x2)+1)` which is fine for straight lines, but will need revisiting for the diagonals.

As I guessed, the diagonal behaviour is better defined here. I can't nicely merge my straight line and diagonal behaviours, so I'm using the `isStraight` method to decide which draw method to use. After my inital implementation, I was getting bad results for the test date, so I implenented a map renderer to see what's going wrong. After further investigation, it would appear I just hadn't committed some changes. It's not so obvious what's up to date in the jupyter kernal :/

## Day 6: Lanternfish ⭐⭐

Compared to playing bingo witha squid or mapping the hudrothermal vents, part 1 seems really easy. Part 2 is obviously supposed to get us to write more efficient code... but how? Even for the test data, calculating the 256 day value took a long time.

Following [u/Montag__](https://www.reddit.com/r/adventofcode/comments/r9z49j/2021_day_6_solutions/hng4ef3/)'s hint, I rebuilt my algoritm to store the number of fish on a given day's count, rather than individual fish each with their own clock. Clearly a much more efficient system, but I'm a lazy coder.

## Day 7: The Treachery of Whales ⭐⭐

A quick check of the test data in excel shows that I need to be looking for the median average, not the mean. A quick google reminded me that python has useful libraries, before I try to roll my own median algorithm, so I'll just import `statistics` and write a one-liner function. Totalling the moves to the median place is also easy.

With the changes in fuel consumption, it seems the median is a better fit. Since I've got `statistics` imported, I'll use their method, rather than impementing my own loop. Also the fuel increase appears to be a triangle number, so I can calculate the costs of a given move with `n(n+1)/2`.  
That's my first **wrong anwer** of the year. Checking the subreddit for clues, I heeded [u/kroppeb](https://www.reddit.com/r/adventofcode/comments/rars4g/2021_day_7_why_do_these_values_work_spoilers/hnk7n2z/)'s advice that the mean finds the best result for *n<sup>2</sup>*, not *n(n+1)/2*. After a quick check of every result for the test data, I can be confident at least that the results are continuous, and there should be just one minimum value.  
After reading more around the subject, it became apparent that the mean should get me close to the correct position, and from there I could just follow the gradient one way or the other.

### Techniques leared

- Incrementor: `+=`
    - Not exactly learning, but when I couldn't use `++` I assumed `+=` was also off limits, until I saw a python snippet today
- `statistics` library probably has some other useful things

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
