[![](https://cloud.drone.io/api/badges/lxbot/adapter-line/status.svg)](https://cloud.drone.io/lxbot/adapter-line)
[![](https://goreportcard.com/badge/github.com/lxbot/adapter-line)](https://goreportcard.com/report/github.com/lxbot/adapter-line)
[![](https://img.shields.io/github/license/lxbot/adapter-line.svg)](https://github.com/lxbot/adapter-line/blob/master/LICENSE)
[![](http://img.shields.io/badge/godoc-reference-5272B4.svg)](https://godoc.org/github.com/lxbot/adapter-line)
[![](https://img.shields.io/docker/image-size/lxbot/adapter-line)](https://hub.docker.com/r/lxbot/adapter-line)

[LINE](https://line.me/ja/)のAdapterです。

- httpアクセス可能な場所で動かす必要があります
- `0.0.0.0:1323`でリッスンします

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_LINE_CHANNEL_SECRET | LINE Developersのチャネル基本設定ページに表示される`チャネルシークレット`をセットします |
| LXBOT_LINE_CHANNEL_ACCESS_TOKEN | LINE Developersのチャネル基本設定ページに表示される`チャネルアクセストークン（長期）`をセットします |