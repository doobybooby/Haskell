# What are Monads

-monad behavior 
-- context means there may or may not be a value
----EX: Maybe is a type of monads. Using the definition above,
----    The context is Maybe, and Maybe has a value of "Just _" or "Nothing".
----    If it is "Just _", you are able to rewrap the value,
----    EX: a = [1,2,3,4],Maybe 2
        Prelude> Just 2 
        If it is "Nothing" there is no value to work with

A monad maybe thought of as an abstracting out a common pattern, or simply an applicative functor. Two main methods you should be aware of are, return and binding. Return, returns the value. Binding (represented by >>=), unwraps a value from a context and allow you to rewrap the value in the same context.

----- EX: examples of monad are, Maybe and IO. Also if you know how to use "do" you are using binding. 


prime exaple is the Maybe function in haskell. It returns "Nothing" 
if the program has Error or the doesn't contain the expected value.
"Just _" key word is used to represent just the value.
