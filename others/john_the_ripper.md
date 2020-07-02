# John

- rockyou.txtをwordlistに

# Usage

```
john --wordlist=/usr/share/wordlists/rockyou.txt pwd.hash
```

すでに解析済みのhashを表示

```
john --show pwd.hash
```

# その他テクニック

- ssh鍵のENCRYPTEDをjohnで解きたい

```
/usr/share/john/ssh2john.py id_rsa > id_rsa.hash
john id_rsa.hash -wordlist=/usr/share/wordlists/rockyou.txt
```
