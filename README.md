# victorialogs-docker
Docker container for VictoriaLogs/Loki experimenting

[VictoriaLogs](https://github.com/faceair/VictoriaLogs) experimentally supports the loki protocol on the VictoriaMetrics Cluster.

More discussion can be found at [VictoriaMetrics# 816](https://github.com/VictoriaMetrics/VictoriaMetrics/issues/816#issuecomment-705538059)

### Usage
```
docker-compose up -d
```

#### Loki Endpoint path:
```
http://127.0.0.1:8481/select/0/
```
#### Loki Insert path
```
http://127.0.0.1:8480/insert/0/loki/api/v1/push
```
#### TCP Insert 
```
$ nc 127.0.0.1 2003
loki{component="parser",level="WARN"} "app log line"
```
