# nmap
言わずと知れたNetwork Discoveryツール

[PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/6a11a6c670b1e016f1536f01fc690e1bc482bd90/Methodology%20and%20Resources/Network%20Discovery.md#nmap)

## usage

```
nmap -sV -sC 10.10.10.180
nmap -sV -sC -p- 10.10.10.180
```

（下は時間がかかるのであまり使わない（が、見逃しが発生するので下もちゃんと実行したほうが良い））

## nmap scripts

### script 検索

```
ls /usr/share/nmap/scripts | grep ldap
```

### Samba
ファイル共有の一覧を列挙
smb-enum-shares.nse
https://nmap.org/nsedoc/scripts/smb-enum-shares.html

リモートの Windows システム上のユーザーを列挙
smb-enum-users.nse
https://nmap.org/nsedoc/scripts/smb-enum-users.html

### nfs
https://nmap.org/nsedoc/scripts/nfs-ls.html

https://nmap.org/nsedoc/scripts/nfs-showmount.html

https://nmap.org/nsedoc/scripts/nfs-statfs.html
