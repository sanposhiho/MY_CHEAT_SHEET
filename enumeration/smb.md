# Samba

### smbmap

```
smbmap -H 10.10.237.52
```

### nmap script
ファイル共有の一覧を列挙
[smb-enum-shares.nse](https://nmap.org/nsedoc/scripts/smb-enum-shares.html)

リモートの Windows システム上のユーザーを列挙
[smb-enum-users.nse](https://nmap.org/nsedoc/scripts/smb-enum-users.html)

```
nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse 10.10.162.244
```

### smbclient
サーバー上の SMB/CIFS リソースにアクセスする

```
smbclient //10.10.162.244/anonymous
```

### smbget
SMB 経由でファイルをダウンロード

```
smbget -R smb://10.10.162.244/anonymous
```

# nfs
正直あんまわかってない
sambaとは別物っぽい？（じゃあここに書くな）

### nmap script

[nfs-ls](https://nmap.org/nsedoc/scripts/nfs-ls.html)

[nfs-showmount](https://nmap.org/nsedoc/scripts/nfs-showmount.html)

[nfs-statfs](https://nmap.org/nsedoc/scripts/nfs-statfs.html)

```
nmap -p 111 -script=nfs-ls,nfs-statfs,nfs-showmount 10.10.162.244
```


### 参考になりそう
[【TryHackMe write-up】kenobi](https://qiita.com/sanpo_shiho/items/4533b514c1e2458015)

[NSEを使った脆弱性調査](http://www.byakuya-shobo.co.jp/hj/moh2/pdf/moh2_p120_p131.pdf)

