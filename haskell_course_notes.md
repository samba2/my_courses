Basics
======
- Haskell only has expressions in contrast to "statements + expressions" in other languages

defintion of a variable:
```
hello name = "Hello, " ++ name
```
concatination operator "++" is separte from addition operator "+"

declaration of a function:
```
sq::Int -> Int -> int   
```
definition of this function
```
sq x y = x * x + y*y
```

Purely functional
=================
- all computation is achieved purely by reducing expressions
- _There are two fundamental operations on functions: function definition (creating a function) and function application (using a function to compute a result)._
- evaluation order does not affect the final value: Church-Rosser theorem
- Haskell programs compute by reduction, i.e. gradually replacing expressions by their values.

Laziness
========
- according to the instructor "laziness" is a distincting feature of Haskell compared to other functional languages.
- _Haskell is "lazy": It only evaluates expressions when they are required for the evaluation of another expression._
- Call by need. Evalution when function parameter is needed
- good for infinite data

Pure and Non-Pure
=================
- _Input and output (I/O) operations are impure. They influence and interact with the ‘outside world’. Essentially, this is the only way to make computers do interesting things._
- the distinction between "pure" and non pure via "I/O" type is a feature unique to Haskell.
- not mixing up pure and unpure: _We know from a function’s type whether it is involved with I/O._
- when I/O is involved, sequencing is important (in constrast to reduction of pure functions which can go multiple paths)


let and where
=============
local scope via `let`
```
  let x = 2
    y = 3
    in x+y
```

`where` as an alternative
```
    squareplusone :: Int -> Int
    squareplusone x = xsquared + 1
     where xsquared = x*x
```

differences:
- `let`
  - these are expressions
  - can be used anywhere an expression is allowed.
- `where` clauses 
  - are not expressions
  - they can be used only to provide some local variables for a top level equation.

guards
======

Alternative to if/then/ else style.
```
absolute x = if (x<0) then (-x) else x
```

with guards becomes 
```
absolute x
  | x < 0 = -x
  | otherwise = x```
```

more complex example:
```
    holeScore :: Int -> Int -> String
    holeScore strokes par
    | score < 0 = show (abs score) ++ " under par"
    | score == 0 = "level par"
    | otherwise = show(score) ++ " over par"
    where score = strokes-par
```
You write a boolean followed by the actual function. Evalution falls through.

Parser combinators
==================
- Parser combinators are functions that allow you to combine smaller parsers into bigger ones.
- They are higher-order functions that take functions as arguments and return functions
- A parser combinator library provides both basic parsers (for words, numbers etc.) and combinators.

Partial function
================
Partial function application is more interesting then currying:
```
    sq x y = x*x+y*y
    sq4 = sq 4 -- = \y -> 16+y*y
    sq4 3 -- = (sq 4) 3 = sq 4 3 = 25
```

Type classes
============
Type classes allow to impose restrictions on polymorphic type variables. Type classes express that e.g. a type represents a number, or something that can be ordered.

Type inference is the analysis of code in order to infer its type. It works using type inference rules that generate typings based on the program text.

The Lambda Calculus
===================
The lambda calculus and the Turing machine have exactly the same computational power.
This led to Church’s thesis — that the set of functions that are effectively computable are exactly the set computable by the Turing machine or the lambda calculus.

When you remove the syntactiv sugur (remember whiteboard-video) you can reduce everything down to a function.

Monads
======
describe computations as sequences of steps, and to handle side effects such as state and IO.
better use "do" notation vs. bind notation.

Good links
==========
- [Monads in Pictures](http://adit.io/posts/2013-04-17-functors,_applicatives,_and_monads_in_pictures.html)
- [A Fistful of Monads - good in depth step-by-step examples](http://learnyouahaskell.com/a-fistful-of-monads)
