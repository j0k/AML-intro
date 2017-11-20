# You can test everything everywhere

# You can generate code by lingvo abstraction both by data example

For example you get data via web stream:
```
{"a":1, "b":3, "c":6}
```

you can catch such packet and the said:
```
obj as class Alphabet
for each field in obj:
  gen method {field.i}X{field.j} that will mult {field.i} x {field.i}
```

then you can:
```
while e:Alphabet in stream:
  print e.aXb()  
```

```[principle] Code abstraction by world real data```
