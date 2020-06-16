# Other Technic

### 引用符に囲まれていないファイル
- [引用符で囲まれていないプログラムパスの処理問題](http://www.sec-pro.net/newsletter/20121112.html)
- PowerUPなどで`CanRestart: True`となってたら置き換え&restartで任意実行可能かも
- [【TryHackMe write-up】Steel Mountain](https://qiita.com/sanpo_shiho/items/9fca52366411c4c4a32e)

### 怪しい特権
特権に関しては[こちら](https://www.exploit-db.com/papers/42556)参照
特権使ったTryHackMeは[これ](https://qiita.com/sanpo_shiho/items/3f2c4595f20cd4133ab8)

- SeImpersonatePrivilege
- SeAssignPrimaryPrivilege
- SeTcbPrivilege
- SeBackupPrivilege
- SeRestorePrivilege
- SeCreateTokenPrivilege
- SeLoadDriverPrivilege
- SeTakeOwnershipPrivilege
- SeDebugPrivilege

### fileの権限
dirの権限を持っていればdir内のfileの権限を変更可能

権限の確認

```
icacls file_name
```

権限の変更

```
icacls root.txt /grant username:F
```

(F = full access) ※権限周りは[これ](https://docs.microsoft.com/ja-jp/windows-server/administration/windows-commands/icacls)を参照

参考: https://qiita.com/sanpo_shiho/items/1857c837b079a7a75db0#pe
