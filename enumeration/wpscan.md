# wpscan
wordpressの脆弱性診断ツール
ユーザーのBrute forceとかもできる

https://github.com/wpscanteam/wpscan

# Usage

一気に色々スキャン

```
wpscan --url http://10.10.10.10 --api-token ***********************
```

apitokenはここから確認
https://wpvulndb.com/users/edit


ユーザーのenum

```
wpscan --url http://10.10.10.10 --enumerate u
```

見つかったUserに対してパスワードのbruteforce

```
wpscan --url http://10.10.10.10  -P /usr/share/wordlists/rockyou.txt
```

※rockyouは時間がかかりすぎる

# 参考になりそう

- https://www.denet.ad.jp/technology/2013/11/vol7-wpscanwordpress.html
- https://blog.sucuri.net/2015/12/using-wpscan-finding-wordpress-vulnerabilities.html
