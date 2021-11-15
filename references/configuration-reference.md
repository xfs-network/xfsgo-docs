# Configuration Reference

The configuration file format is as follows:

```yaml
rpclient:

  # RPC client'address to access gateway.
  # daemom is not affected by this config option.
  # only for other cmd cliends'address to access gateway.
  # usage format：<protocol>://<ip>:<port>
  # default: http://127.0.0.1:9012
  apihost: "http://127.0.0.1:9012"
  # timeout of RPC request
  # default: 180s
  timeout: "180s"

rpcserver:
  # Listening address for JSON-RPC server
  # By default, it will be bound to the local loopback address: 127.0.0.1:9012
  # if need to map outside network you can set [ip]:<port>
  # which port bound support http/s、websocket（ws）protocols
  listen: "127.0.0.1:9012"

p2pnode:
  # address of node in p2p network to listen services of p2p network.
  # By default, it will be bound to the local loopback address: 127.0.0.1:9011
  # if need to map outside network you can set [ip]:<port>
  listen: "0.0.0.0:9011"
  # bootstrap Node in p2p network
  # By default, boostrap list can be obtained by hardcode in xfsgo according to net protocol.
  # bootstrap: []

protocol:
  # protocol version
  version: 1
  # unique id of network protocols
  networkid: 1

miner:
  # address to receive rewards by creating block for xfs blockchain
  # ,which will affect the HASH RATE cause an address represents a node joined in to mine at least
  # by default,a private key will be created by a random number in your local wallet when the xfs blockchain starts for the first time. 
  # you can check your wallet list after the daemon is executed.
  coinbase: ""
  # number of thread executed
  # that will be limited by your mining machine configuration
  numworkers: 10

storage:
  # path of data storage
  # default: $HOME/.xfsdb
  # you can customize this configuration option according to your actural machain env.
  datadir: ""
  # path of block storage
  # default: ${dbdir}/chain
  chaindir: ""
  # path of world state storage
  # default: ${dbdir}/state
  statedir: ""
  # path of keystore storage
  # default: ${dbdir}/keys
  keysdir: ""
  # path to store extra data
  # default: ${dbdir}/extra
  extradir: ""
  nodesdir: ""
# logger level
logger:
  level: "INFO"
```
