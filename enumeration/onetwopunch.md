# onetwopunch
nmapとunicornscanでポートをいい感じにscanしてくれる

https://github.com/superkojiman/onetwopunch

# Usage

```
sudo ./onetwopunch.sh -t targets.txt -p all
```

targets.txtはスキャンしたいIPアドレスのリスト

# 注意

Hack the Boxでは`Send exiting main didnt connect, exiting: system error Interrupted system call`のエラーでこけるので使用できない

OSCPの試験など、他にも使用できないタイミングがあるぽいので使用のタイミングに注意

ref: https://github.com/superkojiman/onetwopunch/issues/5
