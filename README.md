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
how to create a linked list

EX:
5 : [] 
returns: [5]

EX:
5:4:3[]
returns [5,4,3]

### .. (range)
returns the range between two elements


EX:
let numbers = [1..10]
numbers 
returns: [1,2,3,4,5,6,7,8,9,10]


EX:
let numbers = ['a'.. 'g']
numbers 
returns: "abcdefg"

EX:
let numbers = [2,4..10]
numbers 
returns: [2,4,6,8,10]


### head 
returns the first element of the list

EX: 
let numbers = [1,2,3,4,5]
head numbers
returns: [1]

### tail
returns the list except for the first element

EX:
let numbers = [1,2,3,4,5]
tail numbers
returns: [2,3,4,5]

EX:
let numbers = [1,2,3,4,5]
99: tail numbers
returns: [99,2,3,4,5]


EX:
let numbers = [1,2,3,4,5]
15:42:99: tail numbers
returns: [15,42,99,2,3,4,5]


### lenght
returns the lenght of the list

EX:
let numbers = [1,2,3,4,5]
lenght numbers
returns: 6

### reverse 
returns the reverse order of the list

EX:
let numbers = [1,2,3,4,5]
reverse numbers
returns: [5,4,3,2,1]

### !!- index
returns the element of the index

EX:
let numbers = [1,2,3,4,5]
numbers !! 3
returns: [4]

### last
returns the last element of the list

EX:
let numbers = [1,2,3,4,5]
last numbers
returns: 5

### init 
returns everything but the last element

EX:
let numbers = [1,2,3,4,5]
init numbers
returns: [1,2,3,4]


### null 
checks if the given list is empty

EX:
let numbers = [1,2,3,4,5]
null numbers
returns: False

EX:
null []
returns: True

### elem
checks if the given element is in the list

EX:

EX:
let numbers = [1,2,3,4,5]
elem 15 numbers
returns: False


### ++ (concatinator)
concatinates two list


EX:
let numbers = [1,2,3,4,5]
let cucumbers = [55,44,33,22,11]
numbers ++ cucumbers
returns: [1,2,3,4,5,55,44,33,22,11]

### strings == list of characters

EX:
['H','e','l','l','o']
returns: "Hello"

### < && > (check alphabet order)
compaers ascii, lexigraphic
EX:
"adam" < "banana"
returns: True

EX:
"app" > "apple"
returns False;

### maximum 
returns the maximum element within the list

EX:
let numbers = [1,2,3,4,5]
maximum numbers
returns: 5

### minimum
returns the minimum element within the list

EX:
let numbers = [1,2,3,4,5]
minimum numbers
returns: 1

### list inside list [[][]]
you can make a list of lists

EX: 
let numbers = [1,2,3,4,5]
let cucumbers = [6,7,8,9,10]
let apples = [numbers,cucumbers]
apples
returns: [[1,2,3,4,5],[6,7,8,9,10]]

### sum
returns the total sum of the list

EX:
let numbers = [1,2,3,4,5]
sum numbers
returns: 15

### product 
returns the total product of the list


EX:
let numbers = [1,2,3,4,5]
product numbers
returns: 120







### CABAL
