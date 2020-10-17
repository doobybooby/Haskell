# Learn Either
Lets say you have some data type, 

 <some data>
      |
      |
     / \
 Left   Right
  /       \
Int      String

## This can be written in Haskell as 
```Haskell
data SomeData = Left Int | Right String
```

```Haskell
data Either a b = Left a | Right b
```

```Haskell
type SomeData = Either Int String
```
