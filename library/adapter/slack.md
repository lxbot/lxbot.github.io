[![](https://cloud.drone.io/api/badges/lxbot/adapter-slack/status.svg)](https://cloud.drone.io/lxbot/adapter-slack)
[![](https://goreportcard.com/badge/github.com/lxbot/adapter-slack)](https://goreportcard.com/report/github.com/lxbot/adapter-slack)
[![](https://img.shields.io/github/license/lxbot/adapter-slack.svg)](https://github.com/lxbot/adapter-slack/blob/master/LICENSE)
[![](http://img.shields.io/badge/godoc-reference-5272B4.svg)](https://godoc.org/github.com/lxbot/adapter-slack)
[![](https://img.shields.io/docker/image-size/lxbot/adapter-slack)](https://hub.docker.com/r/lxbot/adapter-slack)

[Slack](https://slack.com)のAdapterです。

- [https://api.slack.com/apps](https://api.slack.com/apps) でSlackアプリを作成する必要があります
- `OAuth & Permissions - Scopes`に`chat:write`と`users.profiles:read`を設定する必要があります
- `Subscribe to bot events`に`app_mention`と`message.channels`を設定する必要があります

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_SLACK_OAUTH_ACCESS_TOKEN | botユーザーの`OAuth Access Token`をセットします |
| LXBOT_KOKOROIO_CALLBACKSECRET | botユーザーの`App Credentials - Signing Secret`をセットします |