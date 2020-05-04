## 動かすだけ

```yaml
---
version: "3.6"
services:
  lxbot:
    image: lxbot/lxbot:latest
    environment:
      - LXBOT_MONGODB_URI=mongodb://mongo:27017
      - LXBOT_KOKOROIO_ACCESSTOKEN=
      - LXBOT_KOKOROIO_CALLBACKSECRET=
    networks:
      - wan
      - lan
    ports:
      - 1323:1323
    volumes:
      - adapter:/lxbot/adapters
      - store:/lxbot/stores
      - script-debug:/lxbot/scripts/debug
    depends_on:
      - mongo
    restart: on-failure
  adapter:
    image: lxbot/adapter-kokoro.io
    volumes:
      - adapter:/lxbot/adapters
  store:
    image: lxbot/store-mongodb
    volumes:
      - store:/lxbot/stores
  script-debug:
    image: lxbot/script-debug
    volumes:
      - script-debug:/lxbot/scripts
  mongo:
    image: mongo:4.0
    networks:
      - lan
    volumes:
      - mongo-db:/data/db
      - mongo-configdb:/data/configdb
    restart: on-failure
volumes:
  mongo-db:
  mongo-configdb:
  adapter:
  store:
  script-debug:
networks:
  wan:
  lan:
    internal: true
```

## 開発

- go 1.12以降の環境が必要です