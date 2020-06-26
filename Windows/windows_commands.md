# Windows

### fileの発見
```
dir flag* /s /p
```

### スクリプト実行

```
.\filename
```

### powershellでプロセス実行

```
powershell "Start-Process "sheshe.exe""
```

### serviceのリスタート
```
sc stop AdvancedSystemCareService9
sc start AdvancedSystemCareService9
```

### groupにユーザーの追加

```
net group test_group test_user /add
```

### 現在のユーザーの権限一覧
```
whoami /priv
```
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
