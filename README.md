# rename-terminal
To rename the bash terminal in Ubuntu 20.04

> vim ~/.bashrc

```
#Custome Title of the terminal function
function set-title() {
  if [[ -z "$ORIG" ]]; then
    ORIG=$PS1
  fi
  TITLE="\[\e]2;$*\a\]"
  PS1=${ORIG}${TITLE}
}
```
>source ~/.bashrc

>set-title `whatever-name-you-want`
