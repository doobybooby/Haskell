# What are Monads

-monad behavior 
-- context means there may or may not be a value
----EX: Maybe is a type of monads. Using the definition above,
----    The context is Maybe, and Maybe has a value of "Just _" or "Nothing".
----    If it is "Just _", you are able to rewrap the value,
----    
        Prelude> Just 2 
        If it is "Nothing" there is no value to work with

A monad maybe thought of as an abstracting out a common pattern, or simply an applicative functor. Monads unwraps a value from a context and allow you to rewrap the value in the same context. Two main methods you should be aware of are, return and binding. Return, returns the value. Binding (represented by >>=). Monad gives you a Kleisli composition

----- EX: examples of monad are, Maybe and IO. Also if you know how to use "do" you are using binding. 
```
Old Composition
A -> B--\
         |-- A -> C
B -> C--/


Kleisli composition
A -> M(B)--\
            |-- A-> M(C)
B -> M(C)--/
```


