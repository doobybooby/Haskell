Haskell Environment

progname arg1 arg2

* How do we access arguments?
* What about environment variables?
* What about exit codes?

getProgName to access the progname

getArgs to access the arguments

getEnvironment to access all the environment

lookupEnv uses a Key, then return IO(Maybe String)

withArgs allows users to modify argument 

withProgName allows users to modify progname


```Haskell
# always call exit failure with some int bigger than 0
data EitCode = ExitSuccess | ExitFailure Int
# to exit
exitWith :: ExitCode -> IO a 
exitFailure :: IO a 
exitSuccess :: IO a 
# die is similar to throwing exception 
die :: String -> IO a
```
