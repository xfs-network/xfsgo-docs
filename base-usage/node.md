# Node

So far, the xfsgo daemon program has realized that the full nodes in the XFS network are the nodes that store all the data of the xfsgo blockchain and are connected to the blockchain network through P2P. In the blockchain network, all the full nodes are equal, acting as both clients and servers.

### Select network

In order to make XFS network nodes more flexible to adapt to various extended networks, as well as development, debugging and local private chain deployment, xfsgo uses netid to act on node configuration to distinguish different network environments and initialize mutually isolated chain data.

When using xfsgo daemon to start the node, it will default to the main network (main net, id = 1). Of course, the xfsgo program also provides a network environment for developing tests: test net (test net, id = 2). You can start the test network node in the following ways

```
xfsgo daemon --testnet
```

After the node starts, it will continue to try to connect to other nodes on the network until it has a peer. If you enable UPnP on your router or run XFS nodes on an Internet facing server, connections from other nodes will also be accepted.

For the initial startup, the program has built-in boot nodes, which can quickly connect to the network and continuously spread to other nodes of the network. You can use the following command to customize the boot node you need to connect to:

```
xfsgo daemon --bootstrap <node[,node...]>
```

### Local network

XFSGO provides more network expansion options. You can flexibly configure and build local private network nodes.

### Node ID

Node ID is used in XFS network to identify node uniqueness. After the node is started, you can view your node ID in the following ways

```
xfsgo net getid
```

When you need to connect to the specified network node, you must obtain the network ID of the other party in advance and encode the connection path in the following format:

```
xfsnode://<ip>:<port>/?id=<node_id>
```

You can connect to the specified target node with the following command

```
xfsgo net addpeer <peer_path>
```

### RPC Service

Xfsgo node provides fully managed RPC services, adopts json-rpc 2.0 standard, supports HTTP/s and websocket protocol access, and is bound to the local port 9012 by default. You can package the port according to the security specification and publish it.

{% hint style="warning" %}
RPC service has full access to nodes, including wallet and node status. For the sake of your asset security and system security and stability, please standardize your security measures. If it is not necessary, please do not publish your RPC port
{% endhint %}
