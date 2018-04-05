# Loop Vars

Loop Variables
```
for ...
  changed = (e > el) ^ order
  order = (e > el)
  if changed ...

or

for ...
  order = (e > el)
  changed = lastorder ^ order
  lastorder = order
  if changed ...

```
same as:
```
for ...
  order = e > el
  changed = order ^ order:last
  if changed ...

or

for ...
  order = e > el
  changed = order:changed
  if changed:

or

for ...
  order = e > el
  if order:changed ...

```

var categories:
```
  order:last:1 == order:last
  order:last:N

  order:changed
```
