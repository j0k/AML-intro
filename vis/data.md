# Data Structure visualization info  

After the run examples of data structures would be available to observe:

It is useful to observe:
* structure
* structure + values

Classic example:
```
d = [{'id':1, 'name':"Bob"}, {'id':2, 'name': "Alica"}]
names = map(lambda x:x['name'], d)
```

In VIS mode you choose **name** field and left '}' indent and IDE will suggest you to
generate such queries like:
```
names = map(lambda x:x['name'], d)
```

The main help at the the first will come from:
* you put mouse over var **X** at will see it's structure (in some place:)
  * there you can see examples of **X** variables and *save* the best for the future.
