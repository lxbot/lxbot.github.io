[![](http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square)](https://godoc.org/github.com/lxbot/adapter-slack)

[Slack](https://slack.com)のAdapterです。

- [https://api.slack.com/apps](https://api.slack.com/apps) でSlackアプリを作成する必要があります
- `OAuth & Permissions - Scopes`に`chat:write`と`users.profiles:read`を設定する必要があります
- `Subscribe to bot events`に`app_mention`と`message.channels`を設定する必要があります

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_SLACK_OAUTH_ACCESS_TOKEN | botユーザーの`OAuth Access Token`をセットします |
| LXBOT_KOKOROIO_CALLBACKSECRET | botユーザーの`App Credentials - Signing Secret`をセットします |