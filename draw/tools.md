# IDE have to implement draw tools

## [tool-cmp] compare text/code tool

you can compare any two fragments in will see the difference

```
for(int i=0; i<w-1; i++){
  line(i, ya[i], i+i, ya[i+1]);    
}
```
look like
```
for(int i=0; i<w-1; i++){
  line(i, ya[i], i+1, ya[i+1]);
}
```
[source](https://www.openprocessing.org/sketch/751512)

but they are different.

## codestyle floating

```
 code_i = int_x + 2;

 // you select it

 veryGood(helloWorldVar)

 // --> translate to

 very_good(hello_world_var)
```
