---
id: ou63e199bfw1q5yuuhcou2o
title: Starting Out
desc: ''
updated: 1736551207843
created: 1736522104495
tags:
    - book.chapter
    - coding.haskell
---
[Chapter](https://learnyouahaskell.com/starting-out)

## Ready, set, go!
- Use ghci for interactive Haskell
- Regular infix math notation
    - Use parens around negative numbers
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
