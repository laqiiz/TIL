# bash

return code of grep command.

```sh
# find and return code zero
$ echo "aaa" | grep a
aaa
$ echo $?
0

# not found and return code "1"
$ echo "aaa" | grep 111
$ echo $?
1
```
