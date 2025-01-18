---
id: ou63e199bfw1q5yuuhcou2o
title: Starting Out
desc: ''
updated: 1737226900797
created: 1736522104495
tags:
  - book.chapter
  - coding.haskell
---
[Chapter](https://learnyouahaskell.com/starting-out)

## Ready, set, go!
- Use ghci for interactive Haskell
- Regular infix math notation
    - Use `()` around negative numbers
- Boolean algebra
    - `True` and `False` are bools
    - `&&` is `and`
    - `||` is `or`
    - `not` negates
- Test for equality with `==`
    - Test for inequality with `/=`
    - `==` expects left and right side to be the same type of thing
- Most functions use prefix notation.
    - If there are two inputs then you can still use infix notation by surrounding it with backticks
        - e.g. 92 `div` 10 returns 9
- Function application has highest precedence
    - Think of it like having parens around the function and its inputs.
- Specific Functions
    - `succ` function returns the successor to the input
    - `min` and `max` return the lesser or greater of two inputs
    - `div` does integer division

## Baby's first function
```haskell
doubleMe x = x + x
```
- Can be loaded into ghci by running ghci from the location and using `:l baby`

```haskell
doubleUs x y = doubleMe x + doubleMe y
```
- Able to use other functions in defining new functions
    - Don't have to have things in a particular order (due to Haskell's laziness)

```haskell
doubleSmallNumber x = if x > 100
                        then x
                        else x*2
```
- When doing `if` statements in Haskell the `else` part is mandatory since every function must return something.
- An expression is a piece of code that returns a value
    - An `if` statement is an expression becuase it has to return something

```haskell
doubleSmallNumber' x = (if x > 100 then x else x*2) + 1
```
- If we neglected the `()` then the `+ 1` would have only applied if `x` had been less than 100 (after doubling).
- We use `'` on functions to denote that this is a slightly modified version of another function or variable.

```haskell
conanO'Brien = "It's a-me, Conan O'Brien!"
```
- Functions can't begin with uppercase letters.
- A function without any parameters is called a definition

## An intro to lists
- Lists are *homogenous* data structures
    - This means that all of the things in the list have to be the same kind of thing.

```haskell
let lostNumbers = [4,8,15,16,23,42]
```
- Lists are denoted with `[]` and the values are separated by `,`
- In Haskell `"hello"` is just `['h','e','l','l','o']`
    - This means that we can use list functions on strings

```haskell
[1,2,3,4] ++ [9,10,11,12]
"hello" ++ " " ++ "world"
['w','o'] ++ ['o','t']
```
- These return `[1,2,3,4,9,10,11,12]`, `"hello world"`, and `"woot"` respectively
- Using the `++` opperator is expensive since Haskell has to walk through the entire list on the left of the opperator
- `++` requires both parameters to be lists

```haskell
'A':" SMALL CAT"
5:[1,2,3,4,5]
```
- The `:` (cons operator) prepends a single object to a list instantly
- `:` requires the left to be a single object and the right to be a list of that kind of object.