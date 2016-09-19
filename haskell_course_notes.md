- Haskell only has expressions in contrast to "statements + expressions" in other languages

- functions
- in Python
```
def hello(name):
  return "Hello, " + name
```

in haskell:
```
hello name = "Hello, " ++ name
```
concatination operator "++" is separte from addition operator "+"

- types
- C example:
```
int sq(int x, int y) {
    return x* x+y*y*;
}
```

in Haskell:
- declaration:
```
sq::Int -> Int -> int   
```
- definition:
```
sq x y = x * x + y*y

- list syntax like in Python

```


