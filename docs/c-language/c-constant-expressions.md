---
title: "C Constant Expressions | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-language"]
ms.topic: "language-reference"
dev_langs: ["C++"]
helpviewer_keywords: ["constant expressions, syntax", "constant expressions", "expressions [C++], constant"]
ms.assetid: d48a6c47-e44c-4be2-9c8b-7944c7ef8de7
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus"]
---
# C Constant Expressions
A constant expression is evaluated at compile time, not run time, and can be used in any place that a constant can be used. The constant expression must evaluate to a constant that is in the range of representable values for that type. The operands of a constant expression can be integer constants, character constants, floating-point constants, enumeration constants, type casts, `sizeof` expressions, and other constant expressions.  
  
## Syntax  
 *constant-expression*:  
 *conditional-expression*  
  
 *conditional-expression*:  
 *logical-OR-expression*  
  
 *logical-OR-expression* **?**  *expression* **:**  *conditional-expression*  
  
 *expression*:  
 *assignment-expression*  
  
 *expression* **,**  *assignment-expression*  
  
 *assignment-expression*:  
 *conditional-expression*  
  
 *unary-expression assignment-operator assignment-expression*  
  
 *assignment-operator*: one of  
 **= \*= /= %= += -= <\<= >>= &= ^= &#124;=**  
  
 The nonterminals for struct declarator, enumerator, direct declarator, direct-abstract declarator, and labeled statement contain the *constant-expression* nonterminal.  
  
 An integral constant expression must be used to specify the size of a bit-field member of a structure, the value of an enumeration constant, the size of an array, or the value of a **case** constant.  
  
 Constant expressions used in preprocessor directives are subject to additional restrictions. Consequently, they are known as "restricted constant expressions." A restricted constant expression cannot contain `sizeof` expressions, enumeration constants, type casts to any type, or floating-type constants. It can, however, contain the special constant expression `defined (`*identifier*`)`.  
  
## See Also  
 [Operands and Expressions](../c-language/operands-and-expressions.md)