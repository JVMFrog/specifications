AsmBuilder - bildet VASM code

```java
AsmBuilder builder = new  AsmBuilder();

builder.begin();
Function main = builder.beginFunction();
Variable a = main.variable(I32);
Variable b = main.variable(I32);
Value c = a.plus(b);

main.end();


builder.end();
```
