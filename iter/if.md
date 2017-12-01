# IF execute statements

```
econd = if cond: 1 else 0

exprs = {
  a.process(),
  for i in range(10):
    a.fun()
}

exprs[ econd() ]()
```

the same as:

```
if cond:{
  True => expr1,
  else => expr2
}

if cond:{
  for i in range(10):
    a.fun(),

  a.process()
}
```

the same as:

```
exprs = {
  0 => a.process(),
  1 => for i in range(10):
           a.fun()
}[econd()]
```
