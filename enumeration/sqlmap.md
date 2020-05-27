# sqlmap
SQLiが通るときに実行して祈りを捧げていると色々な情報を取り出してくれるすごいやつ。ちなみにOSCPだと使用不可だった気がする。

# Usage

GETのとき

```
python sqlmap.py -u "http://example.jp/search.php?query=1&order=2"
```

POSTの時

```
python sqlmap.py -u "http://example.jp/sql_injection-003.php" --data "ID=1&PWD=2"
```

以下の記事がめちゃめちゃ詳しく載ってる
[sqlmapでSQLインジェクションの検証](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)
