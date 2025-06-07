# localproxy

通信先を変えるためのプロキシ

App Engine のようなデプロイ毎のURLがある開発環境と相性がいい。

## 使い方

1. conf.d/proxy.example.conf を参考に、プロキシ対象ドメインの設定を書く。
2. (HTTPSをプロキシする場合) 証明書をcerts、秘密鍵をprivateディレクトリに配置する。
   - 証明書、秘密鍵まわりはスコープ外
3. `docker compose up -d` で起動する。
4. /etc/hosts を編集し、プロキシ対象ドメインを 127.0.0.1 に向ける。
