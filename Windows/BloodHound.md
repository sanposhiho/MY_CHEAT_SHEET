# BloodHound
Windows Active Directory環境の分析を行える

# Usage

Targetで`SharpHound.ps1`を使用してデータの収集

```
*Evil-WinRM* PS C:\temp> Import-module ./SharpHound.ps1
*Evil-WinRM* PS C:\temp> Invoke-BloodHound -CollectionMethod ACL,ObjectProps,Default -CompressData -RemoveCSV -NoSaveCache
*Evil-WinRM* PS C:\temp> ls


    Directory: C:\temp


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        6/25/2020  11:04 PM          15232 20200625230431_BloodHound.zip
-a----        6/25/2020  11:02 PM         973117 SharpHound.ps1

```

以下Kaliで

```
sudo neo4j console

bloodhound     #(別shellで)
```

これでGUIが起動する

右側のUpload Dataから先ほどのzipファイルをuploadして解析できる
![スクリーンショット 2020-06-26 16 25 06](https://user-images.githubusercontent.com/44139130/85833742-309d1100-b7cd-11ea-8d4f-70adadd56039.png)


## 参考になりそう
- [BloodHoundを使用したWindows Active Directory環境の分析](https://qiita.com/v_avenger/items/56ef4ae521af6579c058)
- [【HackTheBox】Forest - Walkthrough -](https://qiita.com/v_avenger/items/43014e5e34fe491764c8#bloodhound-%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%9F%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E3%81%AE%E5%88%86%E6%9E%90)
