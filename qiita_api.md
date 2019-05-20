# Qiita API v2

## Summary

* 案外APIでできることが少ない
* 特にOrganization周りのAPIが存在しない
  * Organizationに属するユーザを取得するためにはスクレイピングが必要

## API Query Option

| 項目                                | オプション          |
|-------------------------------------|---------------------|
| タイトルに「2015」を含んでいる      | title:2015          |
| 本文に「Qiita」を含んでいる         | body:Qiita          |
| コードに「Ruby」を含んでいる        | code:Ruby           |
| 「Ruby」タグが付いている            | tag:Ruby            |
| sampleuserが作成した                | user:sampleuser     |
| 「tag:Ruby」を含まない              | -tag:Ruby           |
| 3件より多くストックされている       | stocks:>3           |
| 2015-10-09以降に作成された          | created:>2015-10-09 |
| 2015-10-01 以降に更新された         | updated:>2015-10    |
| 「Ruby」または「Rails」を含んでいる | Ruby OR Rails       |

* [qiita-search-options](https://help.qiita.com/ja/articles/qiita-search-options)
  * Maybe cannot specify hour/minute/second unit

## Link

* https://qiita.com/api/v2/docs


