## 重学 JavaScript

- 乔姆斯基谱系：是计算机科学中刻画形式文法表达能力的一个分类谱系，是由诺姆·乔姆斯基于 1956 年提出的。它包括四个层次：

  - 0- 型文法（无限制文法或短语结构文法）包括所有的文法。
  - 1- 型文法（上下文相关文法）生成上下文相关语言。
  - 2- 型文法（上下文无关文法）生成上下文无关语言。
  - 3- 型文法（正规文法）生成正则语言。

- 产生式：在计算中指 Tiger 编译器将源程序经过词法分析和语法分析后得到的一系列符合文法规则的语句
- 巴科斯诺尔范式，即巴科斯范式(BNF)，是一种用于表示上下文无关文法的语言。
- 终结符：最终在代码中出现的字符

- 用尖括号括起来的名称来表示语法结构名
- 语法结构分成基础结构和需要用其他语法结构定义的复合结构
  - 基础结构称终结符
  - 复合结构称非终结符
- 引号和中间的字符表示终结符
- 可以有括号
- `*` 表示重复多次
- `|`表示或
- `+`表示至少一次

四则运算：

- 1 + 2 \* 3
  终结符：
- Number
- `+ - * /`
  非终结符：
- MultiplicativeExpression
- AdditiveExpression

## 通过产生式理解乔姆斯基谱系

- 0 型 无限制文法
  - `?::=?`
- 1 型 上下文相关文法
  - `?<A>?::=?<B>?`
- 2 型 上下文无关文法
  - `<A>::=?`
- 3 型 正则文法
  - `<A>::=<A>?`
  - `<A>::=?<A>` 错误

JavaScript 是什么语法？
大部分是上下文无关文法，符合正则表达式的是正则文法。

有两个特例:

```
2**1**2, 乘方
是右结合文法，
结果为2
正则文法是左结合。
```

```
{
    get a {return 1},
    get: 1
}
get a 代表属性，get:1 是直接赋值
```

严格上来说，JavaScript 是上下文相关文法。

## 其它产生式

EBNF ABFN Customized

## 现代语言分类

- 形式语言——用途
  - 数据描述语言
    JSON、HTML、CSS、SQL、XAML、YAML
  - 编程语言
    C、C++、Java、C#、python、JavaScript、Ruby、Perl、Lisp、T-SQL、Clojure、Hask、PHP、Lua、SmallTalk、VB、Delphi、Dart
- 形式语言——表达方式
  - 声明式语言
    JSON、HTML、XAML、SQL、CSS、Lisp、Clojure、Haskell
  - 命令型语言
    C、C++、Java、C#、Python、Ruby、Perl、JavaScript、Dart

## 图灵完备性

- 命令式——图灵机
  - goto
  - if 和 while
- 声明式——lambda
  - 递归

## 动态与静态

- 动态
  - 在用户的设备/在线服务器上
  - 产品实际运行时
  - Runtime
- 静态
  - 在程序员的设备上
  - 产品开发时
  - Compiletime

## 类型系统

- 动态类型系统与静态类型系统
- 强类型与弱类型
  - String + Number
  - String == Boolean
- 复合类型
  - 结构体
  - 函数签名
- 子类型
- 泛型
  - 逆变/协变

## 一般命令式编程语言

- Atom
  - Indentifier
  - Literal
- Expression
  - Atom
  - Operator
  - Punctuator
- Statement
  - Expression
  - keyword
  - Punctuator
- Structure
  - Function
  - Class
  - Process
  - Namespace
- Program
  - Program
  - Module
  - Package
  - Library

语法 -> 语义 -> 运行时

## Atom

- Grammar
  - Literal
  - Variable
  - Keywords
  - Whitespace
  - Line Terminator
- Runtime
  - Types
  - Execution Context

### Types

- Number
  - IEEE 754 Double Float
    - Sign(1)
    - Exponent(11)
    - Fraction(52)
  - Grammar
    - DecimalLiteral
      - 0
      - 0.
      - .2
      - 1e3
    - BinaryIntegerLiteral
      - 0b111
    - OctalIntegerLiteral
      - 0o10
    - HexIntegerLiteral
      - OxFF
- String
- Boolean
- Object
- Null
- Undefined
- Symbol
