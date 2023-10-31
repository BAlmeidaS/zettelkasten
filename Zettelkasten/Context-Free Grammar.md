---
tags:
  - Russel-n-Norvig-chap-23
---
A *context-free* [[Grammar]] means, broadly, that any rule can be used in any context.

A context-free grammar consists of the following components:

**Terminals ($\displaystyle \large \Sigma$)**: These are the symbols from which strings are formed. They are the *alphabet* of the grammar and cannot be broken down further. In [[Natural Language Processing|NLP]], these might be words or tokens.

**Non-terminals ($\displaystyle \large V$)**: These are placeholder symbols that are used to define the structure of the language and are replaced in the derivation of strings. They are typically denoted by capital letters.

**Production Rules ($\displaystyle \large P$)**: These are rules that define how a non-terminal can be expanded into a sequence of terminals and/or non-terminals. Each production rule is of the form: A→αA→α where AA is a non-terminal and αα is a string of terminals and/or non-terminals.

**Start Symbol ($\displaystyle \large S$)**: One of the non-terminals is designated as the start symbol. When generating strings from the grammar, the derivation starts from this symbol.

![[Pasted image 20231031110248.png]]