# Haskell
Lean how to code haskell.
Haskell is LAZY, unlike object oriented programming
Haskell reads basked on indentation

### Syntax

Types are sets of values
Typeclasses are sets of types

-- is to comment 

To find out what type x is;
:t 'x' 

f :: [Int] -> Int
//function f takes in [int] and returns an Int.

Loop
pattern... **=** result

guard expression
pattern
**|** expression **=** result
**| otherwise =** result

where expression //Can only be used inside a definition, never nested
result **where**
pattern... **=** result

let expression //Can be used anywhere, can be nested 
**let** pattern... **=** result
**in** result

case expression
**case** expression **of** pattern... **->** result

### Download EMACS and GHCI on linux

### boolean expressions 
&& --and
|| -- or
True
False
not

### if and else
Haskell always has to return a value

EX:
random r = if r ==1
              then "r is one"
              else "r is not one"

### let 
to define functions on the fly

EX: let squareAddOne x = x*x+1

squareAddOne 2
returns: 5

squareAddone 3

returns: 10

EX: 
let x = 4
let y = 7

max x y
returns: 7


### map, (a => b) -> [a] -> [b]
takes a function and a list, returns a new list, applies function to each element 

EX: map add1 [1,2,3,4]
returns: [2,3,4,5]

EX: map (max 3) [1,2,3,4,5]
returns: [3,3,3,4,5]

> ### zipWith
combine two list with a funciton

EX: zipWith (+) [1,1,1,2,3] [1,2,3,4,5]
returns: [2,3,4,6,8]

> ### Flip

> ### filter 
takes function and a list. returns list of True elements;

EX: filter (>5) [1..10]
returns: [6,7,8,9,10]

> ### takeWhile
takes a function and a list. returns the elements until the condition fails.

EX: takeWHile (<3) [1,2,3,4,5]
returns: [1,2]

EX: takeWHile (>3) [1,2,3,4,5]
returns: []

### Currying
Taking a function that takes in multiple arguments into tuples of arguments.

EX: sum3 4 5 6 == ((sum3 4) 5 ) 6)

### linked list





### CABAL
