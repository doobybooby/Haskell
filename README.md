# Learn to Haskell

1. Haskell is LAZY
2. Haskell reads based on indentation (like python)

## Types

1. Types are sets of values
2. Typeclasses are sets of types
3. To find out what type x is;

> :t

```
EX:
Prelude>:t 5
5 :: Num p => p
```
```
EX:
Prelude> :t 'c'
'c':: Char
```

## Functions

> f :: [Int] -> Int
> -- function f takes in [int] and returns an Int.

## Comment

* -- is used to comment 
```
-- comment on a line
```

## Loop

###### Loop Expression

```
pattern... = result
```

###### Guard Expression

```
pattern
| expression = result
| otherwise = result
```

###### Where Expression //Can only be used inside a definition, never nested
```
result where
pattern... = result
```
###### Let Expression //Can be used anywhere, can be nested 
```
let pattern... = result
in result
```
###### Case Expression
```
case expression of pattern... -> result
```

## boolean expressions 
```
&& --and
|| -- or
True
False
not
```
## if and else
* Haskell always has to return a value
```
EX:
random r = if r ==1
              then "r is one"
              else "r is not one"
```
## let 
* To define functions on the fly
```
EX: let squareAddOne x = x*x+1

squareAddOne 2
returns: 5

squareAddone 3

returns: 10
```
```
EX: 
let x = 4
let y = 7

max x y
returns: 7
```

## map, (a => b) -> [a] -> [b]
> Takes a function and a list, returns a new list, applies function to each element 
```
EX: map add1 [1,2,3,4]
returns: [2,3,4,5]
```
```
EX: map (max 3) [1,2,3,4,5]
returns: [3,3,3,4,5]
```
###### zipWith
> Combine two list with a funciton
```
EX: zipWith (+) [1,1,1,2,3] [1,2,3,4,5]
returns: [2,3,4,6,8]
```

###### filter 
> Takes function and a list. returns list of True elements;
```
EX: filter (>5) [1..10]
returns: [6,7,8,9,10]
```
###### takeWhile
> Takes a function and a list. returns the elements until the condition fails.
```
EX: takeWHile (<3) [1,2,3,4,5]
returns: [1,2]

EX: takeWHile (>3) [1,2,3,4,5]
returns: []
```
## Currying
* Taking a function that takes in multiple arguments into tuples of arguments.
```
EX: sum3 4 5 6 == ((sum3 4) 5 ) 6)
```
## linked list
* How to create a linked list
```
EX:
5 : [] 
returns: [5]

EX:
5:4:3[]
returns [5,4,3]
```
###### .. (range)
* Returns, the range between two elements
```

EX:
let numbers = [1..10]
numbers 
returns: [1,2,3,4,5,6,7,8,9,10]
```
```
EX:
let numbers = ['a'.. 'g']
numbers 
returns: "abcdefg"
```
```
EX:
let numbers = [2,4..10]
numbers 
returns: [2,4,6,8,10]
```
```
EX:
let numbers = [10,9..1]
numbers 
returns: [10,9,8,7,6,5,4,3,2,1]
```
```
EX:
let numbers = [2,4..]
numbers 
returns: infinite loop
```
###### head 
* Returns, the first element of the list
```
EX: 
let numbers = [1,2,3,4,5]
head numbers
returns: [1]
```
###### tail
* Returns, the list except for the first element
```
EX:
let numbers = [1,2,3,4,5]
tail numbers
returns: [2,3,4,5]
```
```
EX:
let numbers = [1,2,3,4,5]
99: tail numbers
returns: [99,2,3,4,5]
```
```
EX:
let numbers = [1,2,3,4,5]
15:42:99: tail numbers
returns: [15,42,99,2,3,4,5]
```

###### Lenght
* Returns, the lenght of the list
```
EX:
let numbers = [1,2,3,4,5]
lenght numbers
returns: 6
```
###### reverse 
returns the reverse order of the list
```
EX:
let numbers = [1,2,3,4,5]
reverse numbers
returns: [5,4,3,2,1]
```
###### !!- index
* Returns, the element of the index
```
EX:
let numbers = [1,2,3,4,5]
numbers !! 3
returns: [4]
```
###### last
* Returns, the last element of the list
```
EX:
let numbers = [1,2,3,4,5]
last numbers
returns: 5
```
###### init 
* Returns, everything but the last element
```
EX:
let numbers = [1,2,3,4,5]
init numbers
returns: [1,2,3,4]

```
###### null 
* Checks, if the given list is empty
```
EX:
let numbers = [1,2,3,4,5]
null numbers
returns: False

EX:
null []
returns: True
```
###### elem
* Checks, if the given element is in the list
```
EX:
let numbers = [1,2,3,4,5]
elem 15 numbers
returns: False
```
```
EX:
let numbers = [1,2,3,4,5]
3 `elem` numbers
returns: True
```

###### Concatinator
* "++" is used to concatinates two list
```
EX:
let numbers = [1,2,3,4,5]
let cucumbers = [55,44,33,22,11]
numbers ++ cucumbers
returns: [1,2,3,4,5,55,44,33,22,11]
```
## Strings == list of characters
```
EX:
['H','e','l','l','o']
returns: "Hello"
```
###### < && > (check alphabet order)
* Compares ASCII, lexigraphic
```
EX:
"adam" < "banana"
returns: True
```
```
EX:
"app" > "apple"
returns False;
```
###### maximum 
* Returns, the maximum element within the list
```
EX:
let numbers = [1,2,3,4,5]
maximum numbers
returns: 5
```
###### minimum
* Returns, the minimum element within the list
```
EX:
let numbers = [1,2,3,4,5]
minimum numbers
returns: 1
```
###### sum
* Returns, the total sum of the list
```
EX:
let numbers = [1,2,3,4,5]
sum numbers
returns: 15
```
###### product 
* Returns, the total product of the list

```
EX:
let numbers = [1,2,3,4,5]
product numbers
returns: 120
```
###### take
* Takes the x number of element from the list
```
EX:
let numbers = [1,2..10]
take 5
returns: [1,2,3,4,5]
```
## list inside list [[][]]
* You can make a list of lists
```
EX: 
let numbers = [1,2,3,4,5]
let cucumbers = [6,7,8,9,10]
let apples = [numbers,cucumbers]
apples
returns: [[1,2,3,4,5],[6,7,8,9,10]]
```
## list comprehension
* Expression | variable values, conditions/constraints
```
EX:
[2^n | n <- [1..5]]
returns: [2,4,8,16,32]
```
```
EX:
let numbers = [1,2,3,4,5]
[2^n | n <- numbers]
returns: [2,4,8,16,32]
```
```
EX: -- return, 2 to the power of n | while n is 1-5 , as long as 2^n <10
[2^n | n <- [1..5], 2^n<10]
returns: [2,4,8]
```
```
EX: -- removes the letter r from any given word
[x | x <- "horse", not (elem x "r")]
returns: "hose"
```
```
EX: -- removes the letter r from every word in a list
[x | x <- word, not (elem x "r")] **| word <- ["horse", "marry", "roar"]**
returns: "hose"
```
```
EX: -- takes two different arguments
[[x * y | y <- [1..5]] | x <- [1..5]]
returns: [1,2,3,4,5], [2,4,6,8,10], [3,6,9,12,15], [4,8,12,16,20], [5,10,15,20,25]
```
### drop
### cycle
### repeat
### replicate



### CABAL
