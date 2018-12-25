# RocketMQ Docker

## 配置hosts文件 (注意修改ip)(域名在.env文件中)(可选)

- `192.168.16.240 namesrv.rocketmq.com`
- `192.168.16.240 m.a.broker.rocketmq.com`
- `192.168.16.240 s.a.broker.rocketmq.com`
- `192.168.16.240 m.b.broker.rocketmq.com`
- `192.168.16.240 s.b.broker.rocketmq.com`
- 修改.env文件中的ROCKETMQ_HM_HOST的IP


## RocketMQ base 

- 可以根据需要调整RocketMQ 内存参数(base/Dockerfile)

## RocketMQ 4.0.0-incubating

- `docker-compose up -d`

## RocketMQ 4.2.0

- `docker-compose up -d`

## RocketMQ Console (注意修改ip)

https://github.com/apache/rocketmq-externals/tree/master/rocketmq-console 
```
docker pull styletang/rocketmq-console-ng
docker run -d -e "JAVA_OPTS=-Drocketmq.namesrv.addr=192.168.16.240:9876 -Dcom.rocketmq.sendMessageWithVIPChannel=false" -p 8080:8080 -t styletang/rocketmq-console-ng
```

## RocketMQ资料

- `https://github.com/apache/rocketmq-externals` 官网仓库列表
- `https://dist.apache.org/repos/dist/release/rocketmq/`


