# Stream examples

```
j0k@j0k-space:~$ jupyter kernelspec list
Available kernels:
  python3    /home/j0k/.local/share/jupyter/kernels/python3
  python2    /usr/local/share/jupyter/kernels/python2
j0k@j0k-space:~$ jupyter kernelspec list | aml -s "~'python3'; $2"
/home/j0k/.local/share/jupyter/kernels/python3
```
or like
```
j0k@j0k-space:~$ jupyter kernelspec list | awk '$0 ~ /python3/{print $2}'
/home/j0k/.local/share/jupyter/kernels/python3
```
