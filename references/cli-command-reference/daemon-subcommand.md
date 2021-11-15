# DAEMON 子命令

### 用法

```
xfsgo daemon [--datadir <filename>] [--netid <number>]
             [--p2paddr <address>] [--rpcaddr <address>]
             [--testnet] [--bootstrap <node1,...>]
```

### 命令选项

*   **--datadir, -d \<filename>**

    设置全局数据目录，默认将在系统用户目录创建
*   **--netid, -n \<number>**

    设置网络 ID，默认不指定为主网（0）
*   **--p2paddr, -p \<addr>**

    设置 P2P 节点服务网络监听地址以及端口，默认：`0.0.0.0:9091`
*   **--rpcaddr, -r \<addr>**

    设置 RPC 服务网络监听地址以及端口
*   **--testnet, -t**

    启动测试网络。该选项将会覆盖 netid 选项设置
*   **--bootstrap \<uri\[,uri...]>**

    指定引导节点。多个节点链接使用逗号分隔

