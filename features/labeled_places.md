# code places with labels

case
```

func fullCheck(obj1, p1, p2){
  if (p1 > 1){
    obj1.method(p1);
    return p1;
  }
  else if (p2>2){
    obj1.method(p1+p2);
    return p2;
  }
  else {
    obj1.method(0);
    return 0;
  }
}
```

you will usually use `fullCheck(o,c1,c2)`

you can do smth like that:
```
f2 = fullCheck

f3 = fullCheck(...) {{
  #<: (p1 > 1)
    {p1 = p1 ^2}
  #>: (p2 > 2)
    {p2 = p2/3}
  #>. else // before return
    {obj1.commit()}
  }}
```

will create f3 like
```
func f3(obj1, p1, p2){
  if (p1 > 1){
    p1 = p1 ^2;
    obj1.method(p1);
    return p1;
  }
  else if (p2>2){
    obj1.method(p1+p2);
    return p2;
    p2 = p2/3;
  }
  else {
    obj1.method(0);
    obj1.commit();
    return 0;
  }
}

```

also you can do the same with:
```
func fullCheck(obj1, p1, p2){
  if (p1 > 1){
    ## case_p1
    obj1.method(p1);
    return p1;
  }
  else if (p2>2){
    ## case_p2
    obj1.method(p1+p2);
    return p2;
  }
  else {
    ## caseEnd
    obj1.method(0);
    return 0;
  }
}
```

and
```
f3 = fullCheck(...) {{
  #<: #case_p1
    {p1 = p1 ^2}
  #>: #case_p2
    {p2 = p2/3}
  #>. #caseDef
    {obj1.commit()}
  }}
```

also you can do a lot with any additional constructions:
```
fullCheck(o,p1,p2) : #case_p1: {p1 = p1 ^2}

or

fullCheck(o,p1,p2) : #case_p1: p1 = p1 ^2
```
