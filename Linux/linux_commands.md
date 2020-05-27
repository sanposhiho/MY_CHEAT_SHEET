# Linux commands

### SUIDなファイルを探す

```
find / -perm -u=s -type f 2>/dev/null
```

### バイナリ内の可読な部分を抜き出す

```
strings file
```
