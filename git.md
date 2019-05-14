# Git

## Setup when clone new repository

1. `git config --add user.name laqiiz`
2. `git config --add user.email xxxx@gmail.com`
3. `git remote set-url origin https://<user>:<pass>@github.com/<username>/<repoistory name>.git`

## Cancel git add (staged file)

* `git reset HEAD <target file>`
  * this operation is no change to work code

## Diff in staged file
* `git diff --cached *`

## Cancel git commit

* `git reset --soft HEAR~1`
  * remains work code

## Git push⏫

* `git push origin HEAD`
  * shortcut current branch typing
  * [まだ git push origin するときに current branch 名を入力して消耗しているの?](https://qiita.com/mabots/items/76d48aa33720287253bf)


## Commit history editting✍

1. git rebase -i HEAD~N
  * e.g. git rebase -i HEAD~10
2. edit: `pick` --> `s` or `squash`
3. edit commit message

📢 **CAUTION!!** 📢 

On Windows then use `Git-Bash`!! 

