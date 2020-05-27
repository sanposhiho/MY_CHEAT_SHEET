# nmap
言わずと知れた

## nmap scripts

### script 検索

```
ls /usr/share/nmap/scripts | grep ldap
```

### 種類
#### Samba
ファイル共有の一覧を列挙
smb-enum-shares.nse
https://nmap.org/nsedoc/scripts/smb-enum-shares.html

リモートの Windows システム上のユーザーを列挙
smb-enum-users.nse
https://nmap.org/nsedoc/scripts/smb-enum-users.html

#### nfs
https://nmap.org/nsedoc/scripts/nfs-ls.html

https://nmap.org/nsedoc/scripts/nfs-showmount.html

https://nmap.org/nsedoc/scripts/nfs-statfs.html
