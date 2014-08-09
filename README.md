<!--
scala-syntax-cs
===============

Some Scala syntax for personal use.
-->

# WIP (Work In Progress)

# Scala Syntax Cheat Sheet

## Syntax represented in Extended Backus-Naur Form (EBNF), where:
```
 - | denotes alternative
 - [...] an option (0 or 1)
 - {...} a repetition (0 or more)
```

## Tpes
```
Type = SimpleType | FunctionType

FunctionType = SimpleType '=>' Type | '(' [Types] ')' '=>' Type

SimpleType = Identifier

Types = Type {',' Type}
```
**A type can be:**

- A **numeric type**: ```Int, Double (and Byte, Short, Char, Long, Float)```,
- The **Boolean type** with the values ```true``` and ```false```,
- The **String type**,
- A **Function type**, like ```Int => Int, (Int, Int) => Int```

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

**Expressions can be:**

- An **identifier** such as **_x_**, **_isGoodEnough_**
- An **identifier** such as ```x, isGoodEnough```
- A **literal**, like **_0_**, **_1.0_**, **_"abc"_**
- A **function application**, like **_sqrt(x)_**
- An **operator application** , like **_-x_**, **_y+x_**
- A **selection**, like **_math.abs_**
- A **conditional expr**, like **_if(x<0) -x else x_**
- A **block**, like **_{val x = math.abs(y); x*2}_**
- An **anonymous function**, like **_x=>x+1_**

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


