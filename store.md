## 概要

`Store` は、ステートフルなScriptを実現するためのモジュールです。  

## インターフェース

- `func Boot(ch *chan map[string]interface{})` (optional)

Adapterが読み込まれ、かつ、 `Set` と `Get` が実装されている場合に実行されます。

`map[string]interface{}` をやりとりするためのchannelのポインターを渡します。  
このchannelは予約されているものであり、現段階では使用していません。

その他に、外部データベースの接続処理を実装しておくことができます。  
実装例は [lxbot/store-mongodb/store.go](https://github.com/lxbot/store-mongodb/blob/master/store.go) を参照してください。

- `func Set(key string, value interface{})`

`Script` がKVSに値を設定する場合に実行されます。

- `func Get(key string) interface{}`

`Script` がKVSから値を取得する場合に実行されます。