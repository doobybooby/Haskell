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

### for a monad "M", a value of type "M a" represents having access to a value of type "a" within the context of the monad.

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

### What are monad transformer
You can create a monad with the same functionality of 2 or more monads. 

I.E. if you want a monad to get an IO, then check with a Maybe. You can create a IOMaybe function 

```Haskell
# Always end in "T", such as MaybeT.
# It posses "run___T", such as runMaybeT.
# {run__T :: m (monad a)} returns the monad in the "__T" constructor

newtype MaybeT m a = MaybeT {runMaybeT :: m(Maybe a)}

# return = MaybeT . return . Just
# binding, --> nothing -> return nothing
#           \-> Just y -> runMaybeT (f y)

# instance MonadTrans MaybeT where
#     lift = MaybeT . liftM Just
```






