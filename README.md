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
```
Type = SimpleType | FunctionType

FunctionType = SimpleType '=>' Type | '(' [Types] ')' '=>' Type

SimpleType = Identifier

Types = Type {',' Type}
```
A type can be:

- A **numeric type**: Int, Double (and Byte, Short, Char, Long, Float),
- The **Boolean type** with the values **_true_** and **_false_**,
- The **String type**,
- A **Function type**, like **_Int => Int, (Int, Int) => Int_**

## Expressions

```
Expr = InfixExpr | FunctionExpr | if '(' Expr ')' Expr else Expr

InfixExpr = PrefixExpr | InfixExpr Operator InfixExpr

Operator = identifier

PrefixExpr = ['+'|'-'|'!'|'~'] SimpleExpr

SimpleExpr = identifier | literal | SimpleExpr '.' ident | Block

FunctionExpr = Bindings '=>' Expr

Bindings = identifier[':' SimpleType] | '('[Binding {',' Binding}] ')'

Binding = ident [':' Type]

Block = '{' {Def ';'} Expr '}'
```


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


