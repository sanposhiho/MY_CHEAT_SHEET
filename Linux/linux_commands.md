# Linux commands

### SUIDなファイルを探す

```
find / -perm -u=s -type f 2>/dev/null
```

### バイナリ内の可読な部分を抜き出す

```
strings file
```

### ネットワーク状態確認

```
ss -nltup
```

```
 -t : TCP socketsの表示
 -u : UDP socketsの表示
 -l : listening socketsのみ表示
 -p : socketを使用してるプロセスを表示
 -n : ポート番号をサービス名変換しない(:httpと表示せず:80と表示)
```

https://milestone-of-se.nesuke.com/sv-basic/linux-basic/ss-netstat/
