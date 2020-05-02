[![](http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square)](https://godoc.org/github.com/lxbot/lxlib)

lxlibは `Adapter` や `Script` を開発を補助するライブラリーです。  
`Send`及び`Reply`の引数に渡される`map[string]interface{}`のstructマッピングを行います。  
また、戻り値や`*chan map[string]interface{}`に送るlxbot形式の`map[string]interface{}`を生成します。

## サンプル

### Adapter

```go
func Send(msg M) {
	m, err := lxlib.NewLXMessage(msg)
	if err != nil {
		log.Println(err)
		return
	}
	channelId := m.Room.ID
	message := m.Message.Text
	_ = send(channelId, message)
}

func send(channelId string, msg string) error {
	u := "https://kokoro.io/api/v1/bot/channels/" + channelId + "/messages"

	v := url.Values{}
	v.Set("message", msg)

	req, err := http.NewRequest("POST", u, strings.NewReader(v.Encode()))
	if err != nil {
		return err
	}
	req.Header.Set("X-Access-Token", token)
	req.Header.Set("Content-Type", "application/x-www-form-urlencoded")

	client := &http.Client{}
	resp, err := client.Do(req)
	if err != nil {
		return err
	}
	defer resp.Body.Close()

	return err
}
```

### Script

```go
func OnMessage() []func(M) M {
	return []func(M) M{
		func(msg M) M {
			m, err := lxlib.NewLXMessage(msg)
			if err != nil {
				log.Println("LXMessage error:", err)
				return nil
			}
            handleInternal(m)
            r, err := m.Reply().ToMap()
            if err != nil {
                log.Println("LXMessage error:", err)
                return nil
            }
            return r
		},
	}
}
```