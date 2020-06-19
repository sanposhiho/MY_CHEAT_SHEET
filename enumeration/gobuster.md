# gobuster
dirbusterとどっちが良いのかいまだにわからんけどなんとなくgobuster使うことが多い

# Usage
```
gobuster dir -u http://10.10.10.14 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -k -t 40 -x php,txt
```

## みんなが言ってたお勧めWordlist

- /usr/share/dirb/wordlists/big.txt
- SecLists/Discovery/Web-Content/big.txt
- SecLists/Discovery/Web-Content/common.txt
- SecLists/Discovery/Web-Content/SVNDigger/all.txt
