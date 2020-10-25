## 学习笔记

### regexp

在 Vscode 里追加扩展《Regex Previewer》
可以验证自己写的正规表达式是否正确。

### 四则运算

```
    TokenNumber:
        1 2 3 4 5 6 7 8 9 0的组合
    Operator: +、-、*、/之一
    Whitespace: <SP>
    LineTerminator: <LF> <CR>


    <Expression>::=
        <AdditiveExpresson><EOF>
    <AdditiveExpression>::=
        <MultiplicativeExpression>
        |<AdditiveExpression><+><MultiplicativeExpression>
        |<AdditiveExpression><-><MultiplicativeExpression>
    <MultiplicativeExpression>::=
        <Number>
        |<MultiplicativeExpression><*><Number>
        |<MultiplicativeExpression></><Number>


    <AdditiveExpression> ::=
        <Number>
        |<MultiplicativeExpression><*><Number>
        |<MultiplicativeExpression></><Number>
        |<AdditiveExpression><+><MultiplicativeExpression>
        |<AdditiveExpression><-><MultiplicativeExpression>
```
