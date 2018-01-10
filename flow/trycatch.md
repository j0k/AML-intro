# Controlled try-catch-finally flow


Example
```
[code block MACRO
  try:
    f()
  catch Exc as e:
]

f:
  try:
    g()
  catch Exc as e:
```

The idea of advanced flow control to catch exception for g in MACRO block and then
continue f execution. The real world example:

```
DB_dumper(messages):
  try:
    for m in messages:
      dump(m)
  catch db.DBError as e:
    log(e)

dump(m):
  check(m)
  fields = take(m)
  db.insert(m)
```

In that case we will stop inserting after first exception.

we can make change like:
```
dump(m) out exception db.DBError:
  check(m)
  fields = take(m)
  db.insert(m)  
```

or
```
dump(m) out: [exception db.DBError]:
dump(m) / [exception db.DBError]:
```

and it will correct processing stage.
