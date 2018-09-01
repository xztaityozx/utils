# utils

## cpconv
cp939とcp930のテーブルを利用して難読化するやつ

```sh
$ echo date | ./cpconv # utf-8 => cp930 => cp939 => utf-8
ｴｱﾎｵ
$ echo ｴｱﾎｵ | ./cpconv -d # utf-8 => cp939 => cp930 => utf-8
date
$ echo date | ./cpconv -P # ワンライナーを出力
echo ｵｲﾔｶ | iconv -f utf-8 -t cp939 | iconv -f cp930 -t utf-8 | bash
```
