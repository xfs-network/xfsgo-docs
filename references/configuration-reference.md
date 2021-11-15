# Configuration Reference

配置文件格式如下：

```yaml
rpclient:
  # RPC 客户端网关地址
  # 除了 daemon 守护进程，其他客户端命令需要用到的 RPC 服务网关地址
  # 配置格式：<protocol>://<ip>:<port>
  # 默认值：http://127.0.0.1:9012
  apihost: "http://127.0.0.1:9012"
  # RPC 客户端网关超时时间
  # 默认值：180s
  timeout: "180s"
rpcserver:
  # daemon 守护进程启动的 RPC 服务网关地址
  # 默认为：127.0.0.1:9012
  listen: "127.0.0.1:9012"
p2pnode:
  # P2P 节点的服务地址
  # 默认为：0.0.0.0:9011
  listen: "0.0.0.0:9011"
  # P2P 网络服务引导节点
  # 默认硬编码内置
  # bootstrap: []
protocol:
  # 协议版本号
  # 默认为: 1
  version: 1
  # 网络ID
  # 默认为主网：1
  # 可选内置测试网络：2。其他网络请使用额外的数值
  networkid: 1
miner:
  # 设置矿工收益地址
  # coinbase: ""
  # 启动的工作线程数量
  numworkers: 10
storage:
  # 程序相关数据存储路径
  # 默认为：$HOME/.xfsgo
  # windows 系统的默认地址为当前执行目录
  datadir: ""
  # 本地链数据存储路径
  # 默认使用: ${dbdir}/chain
  chaindir: ""
  # 本地状态数据存储路径
  # 默认使用: ${dbdir}/state
  statedir: ""
  # 本地私钥数据存储路径
  # 默认使用: ${dbdir}/keys
  keysdir: ""
  # 额外数据存储路径
  # 默认使用: ${dbdir}/extra
  extradir: ""
  # P2P 网络节点数据存储路径
  # 默认使用: ${dbdir}/nodes
  nodesdir: ""
# 程序日志输出级别
# 默认为 INFO
logger:
  level: "INFO"
```
