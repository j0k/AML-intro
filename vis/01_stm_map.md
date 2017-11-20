# Statement Mapping [IDEA | !IMPL]

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
