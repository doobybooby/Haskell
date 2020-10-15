# Records in haskell

### It is hard for an indiviudal to understand what the String and the Int represents
```Haskell
data Object = Object String Int
```

### So you use a record,
```Haskell
data Object = Object (Var1 :: String,
                      Var2 :: Int}
```

### EX:
```Haskell
data Person = Person String Int
data Person = Person { name :: String,
                       age :: Int} 
```                       
                       
### This is generated automatically
```Haskell
name :: Person -> String
age :: Person -> Int
```

### Adding a function greet to Person
```Haskell
greet :: Person -> [Char]

greet person = "Hi " ++ name person 
# OR, using pattern matching 
greet person (Person name _) = "Hi " ++ name
```

## Records can have multiple constructor
```Haskell
data Point =
    D2 { x :: Int, y :: Int}
  | D3 { x :: Int, y :: Int, z :: Int}
```
       
