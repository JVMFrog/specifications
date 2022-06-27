AsmBuilder - bildet VASM code


This code generate following code

```java
AsmBuilder builder = new  AsmBuilder();

builder.begin();

Const const = builder.const(HALF, "100");
Const const2 = builder.const(HALF, "200");

Function main = builder.beginFunction("main");
Variable a = main.localVariable();
a.load(const);
Variable b = main.localVariable();
b.load(const2);
Value c = a.plus(b);
builder.printi(c.register());
main.end();


builder.end();
```


```asm
.code
global main:
  frame
  mov R0, 100
  mov R1, 200
  add R2, R0, R1
  printi R2
  ret
```
