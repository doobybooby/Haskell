# 1. What are Monads

A monad maybe thought of as an abstracting out a common pattern, or simply an applicative functor. Monads unwraps a value from a context and allow you to rewrap the value in the same context. Two main methods you should be aware of are, return and binding. Return, returns the value. Binding (represented by >>=). Monad gives you a Kleisli 

Monads can be used to avoid boilerplate code by creating its own data type

for a monad "***M***", a value of type "***M a***" represents having access to a value of type "***a***" within the context of the monad.

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
Monads 

# 2. In terms of Relex-FRP





# 3. What are monad transformer

It allows you to create a monad with the same functionality of 2 or more monads. This can be useful, such as combining the IO functionality with a Maybe to check if the user enters a valid input.

```Haskell
# Always end in "T", such as MaybeT.
# It posses "run___T", such as runMaybeT.
# {run__T :: m (monad a)} returns the monad in the "__T" constructor

newtype MaybeT m a = MaybeT {runMaybeT :: m(Maybe a)}

# return = MaybeT . return . Just
# binding, --> nothing -> return nothing
#           \-> Just y -> runMaybeT (f y)

# Lift, take the monad then lift it into a new context
class MOnadTrans t where
        lift :: (Monad m) => m a -> t m a 
```

# 4 What are partial function and total function

Partial function is a function that is not defined for all possible argunments of the specified type. Such as div, it is undefined if the divisor is zero

Total funciton - function which is defined for all inputs of the right type. Such as, square function (x^2). Any number can be squared, and 0^2=1;

# 5. Why a data base is important for a web server

Data base are used to provide data access for authorized users. The data can then be easily accessed, managed, modified, updated, controlled, and organized

# 6. What is an API

API stands for application programming interface, it is simply a messenger that takes user request, tells the system, then deliver the response back to user. API is used everywhere, such as sending an instant message. You are commanding the system to send a message. The system will then check for internet/cellular connection, valid phone numbers, etc, but this is not part of the API. The system will tell you if a message has been delivered, sent if successful, failed if failure.

