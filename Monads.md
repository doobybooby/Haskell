# What are Monads

-abstracting out a common pattern as a definition 
-- monads are just applicative functor 
-monad behavior 
--bind, unwrap a value from context, and allow you to rewrap the value in the same context 
-- context means there may or may not be a value
----EX: Maybe is a type of monads. Using the definition above,
----    The context is Maybe, and Maybe has a value of "Just __" or "Nothing".
----    If it is "Just _", you are able to rewrap the value,
----    EX: a = [1,2,3,4],Maybe 2
        Prelude> Just 2 
        If it is "Nothing" there is no value to work with
        



">>=" known as bind
--- takes a function between two types and produces a function that does the 
"same thing" to value then "flattens" the information into one


prime exaple is the Maybe function in haskell. It returns "Nothing" 
if the program has Error or the doesn't contain the expected value.
"Just" key word is used to extract just the value.

main methods are binding (>>=) or return (return)

Think of monad as a wrapper, very similar to Maybe. 
