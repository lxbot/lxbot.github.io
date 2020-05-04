[![](https://cloud.drone.io/api/badges/lxbot/plugin-help/status.svg)](https://cloud.drone.io/lxbot/plugin-help)
[![](https://goreportcard.com/badge/github.com/lxbot/plugin-help)](https://goreportcard.com/report/github.com/lxbot/plugin-help)
[![](https://img.shields.io/github/license/lxbot/plugin-help.svg)](https://github.com/lxbot/plugin-help/blob/master/LICENSE)
[![](http://img.shields.io/badge/godoc-reference-5272B4.svg)](https://godoc.org/github.com/lxbot/plugin-help)
[![](https://img.shields.io/docker/image-size/lxbot/plugin-help)](https://hub.docker.com/r/lxbot/plugin-help)

Scriptのヘルプを表示するPluginです。  
ロードされているScriptに`func Help() string`が定義されている場合に、`Help()`を実行し、その返り値の文字列をヘルプとして表示します。

## サンプル

以下のような関数をScriptに定義します。

```go
func Help() string {
	return "hoge: ほげを実行します"
}
```