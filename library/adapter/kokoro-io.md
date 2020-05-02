[![](http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square)](https://godoc.org/github.com/lxbot/adapter-kokoro.io)

[kokoro.io](https://kokoro.io)のAdapterです。

- httpアクセス可能な場所で動かす必要があります
- `0.0.0.0:1323`でリッスンします

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_KOKOROIO_ACCESSTOKEN | kokokro.ioのbot設定ページに表示される`Access Token`をセットします |
| LXBOT_KOKOROIO_CALLBACKSECRET | kokokro.ioのbot設定ページに表示される`Callback Secret`をセットします |