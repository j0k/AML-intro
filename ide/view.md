#View Port

Cursor position execute a window to the right. During the navigation via:
Left, Right, Top, Bottom buttons it will show the window on the right.


Example:
```
def f(z):
  return 1.0/(1.0 + math.exp(z))

a = 2
c = f(a)

print "a = {a}, c = {c}"
```

when cursor on a
```

                                         | opt  | opt  |
a                                        |   1  |   3  |
                                         ---------------
                                         | opt  | opt  |
                                         |   2  |   4  |

```


## DateTime Example (View Port)

```
d = Date() to ('UTC') format('%day/%month/%year %hh:%mm:%ss')
print d
```
the same as
```
d = Date().to('UTC').format('%day/%month/%year %hh:%mm:%ss')
print d
```

when your cursor on the word 'format'
```
d = Date().to('UTC').format()                  
                                        | format("%hh:%mm:%ss")       | format("%DD %MONTH %YYYY %hh/%mm/%ss")  |
                                        |                             |                                         |
                                        -------------------------------------------------------------------------
                                        | format("%hh:%mm %M/%D/%Y")  | format("%hh:{%mm}:color(RED) %M/%D/%Y") |
                                        |                             |                                         |
```

# Principle

AML - self necessary for the specific knowledge area. It's helpful and support the dialog
