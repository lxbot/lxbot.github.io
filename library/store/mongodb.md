[![](https://cloud.drone.io/api/badges/lxbot/store-mongodb/status.svg)](https://cloud.drone.io/lxbot/store-mongodb)
[![](https://goreportcard.com/badge/github.com/lxbot/store-mongodb)](https://goreportcard.com/report/github.com/lxbot/store-mongodb)
[![](https://img.shields.io/github/license/lxbot/store-mongodb.svg)](https://github.com/lxbot/store-mongodb/blob/master/LICENSE)
[![](http://img.shields.io/badge/godoc-reference-5272B4.svg)](https://godoc.org/github.com/lxbot/store-mongodb)
[![](https://img.shields.io/docker/image-size/lxbot/store-mongodb)](https://hub.docker.com/r/lxbot/store-mongodb)

[MongoDB](https://www.mongodb.com)のStoreです。  
マネージドサービスの[MongoDB Atlas](https://www.mongodb.com/cloud/atlas)でも使用できます。

## 環境変数

| キー | 概要 |
| ---- | ---- |
| LXBOT_MONGODB_URI | `mongodb://`で始まるmongodbのURIをセットします |