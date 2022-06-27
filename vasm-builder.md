AsmBuilder - bildet VASM code


This code generate following code

```java
AsmBuilder builder = new  AsmBuilder();

builder.begin();

Const const = builder.const(HALF, "100");
Const const2 = builder.const(HALF, "200");

Function main = builder.beginFunction("main");
Variable a = main.variable(I32);
a.load(const);
Variable b = main.variable(I32);
b.load(const2);
Value c = a.plus(b);

main.end();


builder.end();
```


```java
.stack

.code
global main

```
