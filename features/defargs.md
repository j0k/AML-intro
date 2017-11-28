# Default Arguments

```
def f(a = 1.0):
  return 1/(1.0 + math.exp(-a))

f.@a = sys.argv[1] if sys.argv[1]

f()
```

**f()** will be called with with sys.argv[1] if it's defined.

Q: How long context with changed default parameters of f() will be continued?
May be for the next call? Or for current block and all block inside? Or while we not changed it to default?

Options
* for the next call
* during current block and all blocks inside
* while the UNDO modification

```
f(a = sys.argv[1]) if $ok

the same as

f(a = sys.argv[1] if $ok)

the same as

f.@a 1= sys.argv[1] if $ok
f()
```

Options:
```
* for the next call
f.@a 1= sys.argv[1] if $ok

* during current block and all blocks inside
f.@a b= sys.argv[1] if $ok

* while the UNDO modification
f.@a u= sys.argv[1] if $ok
```

So here we introduce statement `verbing` and computational statements parametrization.
