# Target recompulation

For example

We have
```
zsh_wifi_signal(){
    local signal=$(nmcli device wifi | grep yes | awk '{print $8}')
    local color='%F{yellow}'
    [[ $signal -gt 75 ]] && color='%F{green}'
    [[ $signal -lt 50 ]] && color='%F{red}'
    echo -n "%{$color%}\uf230  $signal%{%f%}" # \uf230 is 
}
```

from here [powerlevel9k](https://github.com/Powerlevel9k/powerlevel9k)

where

```
local signal=$(nmcli device wifi | grep yes | awk '{print $8}')
```

is a complex expression to get *power of the wifi signal*.

I see that we have too much computations to get $8

in AML it will be something like:

```
gen f() => x:int
bash($(nmcli device wifi | grep yes | awk '{print $8}')) => result
```
