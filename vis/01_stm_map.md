# Statement Mapping [IDEA | IMPL]

When code JSON objects:
```
some['x'] = b['long_x' ]
some['y'] = b['long_x2']
some['z'] = b['param_3']
```

have the ability to declare:

```
some as JSON
s: $native as some['$native'] :! x,y,z in $native

x = b['long_x' ]
y = b['long_x2']
z = b['param_3']
```

details:
```
s: - statement: (it's about statement replacing)
:! - ONLY WHEN
```

```[lingvo] I also want to use the phrase "Full Visual Reflection".```


## Works with all as simple objects

```
j['qty'] = 1
j['price'] = "1234.56"

def amount(j):
  return j['qty'] * j['price']

print j['qty']
print j['price']
print j['amount']
```
have to be

```
 j as class Trade
 Trade: .amount = .qty * .price : price, qty -> float

 print j.qty
 print j.price
 print j.amount
```

```[principle] Principle: all objects are short, simple for access and easy for editing.```
