# Kali commands
Kaliでの調査用のコマンド達


### バイナリ内の可読な部分を抜き出す

```
strings file
```


### hex dumpの解析

```
cat hype_key | xxd -r > result
```

### base64のencode
こうしないと最後に余計な`/n`が入っちゃう気がする

```
tr -d "\n" < test.txt | base64
```
