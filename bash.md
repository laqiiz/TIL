# bash

return code of grep command.
grepに一致しなかった場合、error状態になる。
Jenkins Scriptでのgroovyでshell実行したときにこの仕様に気が付かずハマった.

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
