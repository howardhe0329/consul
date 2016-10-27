# consul docker
## consul server
启动命令

```
docker run -d --name consul --net=host howardhe/consul-server:0.7.0 agent -server --bootstrap-expect=3 -bind=192.168.99.8 -client=0.0.0.0 -dc=web_app -join=192.168.99.15 -ui -ui-dir=/consul/ui
```
## consul client
启动命令

```
docker run -d --name consul --net=host consul agent -bind=192.168.99.9 -join=192.168.99.15
```
