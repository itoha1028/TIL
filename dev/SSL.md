---
tags:
  - ssl
  - web
---

# OpenSSL

# p12ファイルから証明書を取り出す
```
openssl pkcs12 -in foo.pfx -nocerts -nodes -out sample.cert
```

```
openssl pkcs12 -in foo.pfx -nocerts -nodes -out sample.cert
```

```
wget -S -d --certificate=〜/client.cert --ca-certificate=〜/client.cacert --private-key=〜/client.key http://xyz.com -O -
```

https://jp.globalsign.com/support/faq/07.html

https://qiita.com/cs_sonar/items/f2753ffdebb1c67d5302