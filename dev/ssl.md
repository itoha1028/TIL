---
tags:
  - ssl
  - web
---

# SSL

## OpenSSL

## p12ファイルから証明書を取り出す

```text
openssl pkcs12 -in foo.pfx -nocerts -nodes -out sample.cert
```

```text
openssl pkcs12 -in foo.pfx -nocerts -nodes -out sample.cert
```

```text
wget -S -d --certificate=〜/client.cert --ca-certificate=〜/client.cacert --private-key=〜/client.key http://xyz.com -O -
```

### 証明書ファイルの内容を確認

openssl x509 -text -noout -in /\[FilePath\]/\[CertFile\]

### 秘密鍵ファイルの内容を確認

openssl rsa -text -noout -in /\[FilePath\]/\[KeyFile\]

### CSRファイルの内容を確認

penssl req -text -noout -in /\[FilePath\]/\[CSRFile\]

[https://jp.globalsign.com/support/faq/07.html](https://jp.globalsign.com/support/faq/07.html)

[https://qiita.com/cs\_sonar/items/f2753ffdebb1c67d5302](https://qiita.com/cs_sonar/items/f2753ffdebb1c67d5302)

## 証明書ストアの内容を確認する

keytool -list -v -storepass \[パスワード\] -keystore ./\[ストアファイル\].p12

