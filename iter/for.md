# Different forms of iterations combined with macrosyntaxis

```
data = getData()
pairs = ["BTC", "LTC"]

b = {}
for p in pairs:
  b[p] = data[p]

return {"ret": b}
```

can be

```
pairs = ["BTC", "LTC"]

return b = {}:  
  data = getData()
  p in pairs: b[p] = data[p]  
```

also as

```
pairs = ["BTC", "LTC"]

return b = {}:  
  data = getData()
  pairs: b[$_] = data[$_]    
```

also as
```
pairs = ["BTC", "LTC"]

return b = {}:  
  pairs: b[$_] = data[$_]: data = getData()
```

also as
```
pairs = ["BTC", "LTC"]

return b = {}:  
  pairs: b[$_] = _[$_]: _ = getData()
```
also as
```
return b = {}: ["BTC", "LTC"]: b[$_] = _[$_]: _ = getData()
```
also as
```
expr t a, b, c: a[c] = b[c]  
return b = {}: ["BTC", "LTC"]: t(b,_,$_): _ = getData()
```

```
[target] Also the most interesting thing - to make simple 'for' walking via complex structures.
```

## semantic possibility

in Python we have:
```
a = ["hello", "world", "how", "are", "you"]
for i,e in enumerate(a[-1::-1]):
    print(i,e)

<<<
0 you
1 are
2 how
3 world
4 hello
```

it's good to have an option to see:
```
a = ["hello", "world", "how", "are", "you"]
for e in a[-1::-1]:
  print(e:lp,e)
  print(e:list_position,e)
<<<
4 you
3 are
2 how
1 world
0 hello
```
