[![](https://cloud.drone.io/api/badges/lxbot/adapter-discord/status.svg)](https://cloud.drone.io/lxbot/adapter-discord)
[![](https://goreportcard.com/badge/github.com/lxbot/adapter-discord)](https://goreportcard.com/report/github.com/lxbot/adapter-discord)
[![](https://img.shields.io/github/license/lxbot/adapter-discord.svg)](https://github.com/lxbot/adapter-discord/blob/master/LICENSE)
[![](http://img.shields.io/badge/godoc-reference-5272B4.svg)](https://godoc.org/github.com/lxbot/adapter-discord)
[![](https://img.shields.io/docker/image-size/lxbot/adapter-discord)](https://hub.docker.com/r/lxbot/adapter-discord)

[Discord](https://discordapp.com)のAdapterです。

- [https://discordapp.com/developers/applications](https://discordapp.com/developers/applications)でdiscordアプリケーションを作成する必要があります
- 作成したbotに`OAuth2 URL`のスコープを設定する必要があります

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_DISCORD_BOT_TOKEN | `Discord Bot Token`をセットします |