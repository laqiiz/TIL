# GitHub

## 2-factor-authentification

* public document
  * https://help.github.com/en/articles/securing-your-account-with-two-factor-authentication-2fa
* 2段階認証を有効にするとgit pushする時に失敗してしまう
  * 鍵交換を実施しgitプロトコルを使うとpushできるようになるが、ssh-keygen時に指定したpassを入力するのが手間
  * [access-tokenを生成すると便利](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line)
    * `git remote set-url origin https://laqiiz:<access-token>@github.com/laqiiz/<repository-name>.git` で今まで通りアクセスできた
  
