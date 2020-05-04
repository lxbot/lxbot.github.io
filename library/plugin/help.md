[![](http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square)](https://godoc.org/github.com/lxbot/plugin-help)

Scriptのヘルプを表示するPluginです。  
ロードされているScriptに`func Help() string`が定義されている場合に、`Help()`を実行し、その返り値の文字列をヘルプとして表示します。

## サンプル

以下のような関数をScriptに定義します。

```go
func Help() string {
	return "hoge: ほげを実行します"
}
```