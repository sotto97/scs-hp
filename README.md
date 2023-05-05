# scs-hp

SottoCreativeStudio の公式 HP

# デプロイについての残タスク

```bash
## 現状

Cloudfrontのurlは　https://d1d0y47cnxatfs.cloudfront.net/　でアクセスが可能で
Route53では scs.com というホストゾーンを作成している。

## したいこと

scs.comにアクセスした時に、https://d1d0y47cnxatfs.cloudfront.net/　に遷移するようにしたい
```

## インフラについて

CloudFront + S3 を利用している

S3 をオリジンとして設定する場合、サブドメインに対するインデックスドキュメントが対応できないので、CloudFront Functions を利用してインデックスドキュメント機能を実装する。

```bash
# インデックスドキュメント機能とは
Webサーバーが特定のフォルダへアクセスされた場合に、自動的に表示するファイルを設定する機能のこと。
例えば、ユーザーが https://example.com/ というURLにアクセスした場合に、index.htmlを表示するように設定することができる。

※Apacheではhttpd.confを編集することによって実現することができる機能
```

方法としては、以下 2 通りの方法がある

1. S3 の「静的ウェブサイトホスティング」の機能を使って、URL を発行し、その URL をオリジンとして設定する方法
2. CloudFront のオリジンとして直接 S3 を指定する方法

| URL                                 | 結果       |
| ----------------------------------- | ---------- |
| https://example.com/                | 開ける     |
| https://example.com/index.html      | 開ける     |
| https://example.com/test/           | 403 エラー |
| https://example.com/test/index.html | 開ける     |
