# hansel

## 概要
* DiscordからMinecraftゲームサーバ(EC2)を操作するDiscordBot
* Minecraftゲームサーバ: [gretel](https://github.com/shokkunrf/gretel)

## 機能
* EC2の起動(トリガーメッセージ: start)
* EC2の停止(トリガーメッセージ: sleep)
* EC2のPublicIPAddress確認(トリガーメッセージ: status)

## 使い方
### 必要なもの
* docker-compose

### 事前準備
* EC2インスタンスの作成
* DiscordBotの作成

### clone
```sh
git clone https://github.com/shokkunrf/hansel.git
cd hansel
```

### .envの作成
```
BOT_ID=<DiscordBotのTOKEN>
INSTANCE_ID=<EC2インスタンスid>
AWS_ACCESS_KEY_ID=<EC2にアクセス可能なcredentialsのkey>
AWS_SECRET_ACCESS_KEY=<EC2にアクセス可能なcredentialsのsecret_key>
AWS_DEFAULT_REGION=<EC2インスタンスのリージョン>
AWS_DEFAULT_OUTPUT=json
```

### 実行
```sh
docker-compose up --build -d
```
