<!--
scala-syntax-cs
===============

Some Scala syntax for personal use.
-->

# WIP (Work In Progress)

# Scala Syntax Cheat Sheet

## Syntax represented in Extended Backus-Naur Form (EBNF), where:
 - | denotes alternative
 - [...] an option (0 or 1)
 - {...} a repetition (0 or more)

## Tpes

Type = SimpleType | FunctionType

FunctionType = SimpleType '=>' Type | '(' [Types] ')' '=>' Type

SimpleType = Ident

Types = Type {',' Type}




## References

```
Coursera
Martin Odersky.
Functional Programming Principles in Scala
[Online] Available from: https://class.coursera.org/progfun-003
[Accessed: 06 August 2014].

Coursera
Martin Odersky.
Functional Programming Principles in Scala.
Lecture 2.4 - Scala Syntax Summary (4:13).
[Online] Available from:https://class.coursera.org/progfun-003/lecture/41
[Accessed: 06 August 2014].

Scala
[Online] Available from: http://www.scala-lang.org/
[Accessed: 06 August 2014].

Extended Backus–Naur Form
[Online] Available from: http://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_Form
[Accessed: 09-08-2014]
```


