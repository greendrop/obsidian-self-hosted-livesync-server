# Obsidian Self-hosted LiveSync Server

[Obsidian Self-hosted LiveSync](https://github.com/vrtmrz/obsidian-livesync) で使用する CouchDB を構築するための Docker Compose ファイルです。

参考: https://github.com/vrtmrz/self-hosted-livesync-server

## 環境

- Docker

NOTE: Cloudflare Tunnel を使用する想定のため、Nginx や Caddy などのリバースプロキシは使用しません。

## セットアップ

### リポジトリをクローン

```bash
git clone git@github.com:greendrop/obsidian-self-hosted-livesync-server.git
cd obsidian-self-hosted-livesync-server
```

### `.env` ファイルを作成

```bash
cp .env.example .env
```

### `.env` ファイルを編集

`COUCHDB_USER` と `COUCHDB_PASSWORD` を適切な値に変更します。

```
COUCHDB_USER=testuser
COUCHDB_PW=testpassword
```

### Docker Compose を起動

```bash
docker-compose up -d
```

### CouchDB にアクセス

ブラウザで CouchDB の管理画面にアクセスします。
ユーザー名とパスワードは `.env` ファイルで設定した値を使用します。

```
http://localhost:5984/_utils/
```
