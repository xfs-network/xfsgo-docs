# 本地链管理

在节点运行过程中，不管是来自于网络的同步数据，或者本地封装的区块，都将会在本地产生历史的区块数据。您可以使用 `chain` 命令查看本地的历史链数据。例如：你可以通过以下命令查看本地的最新区块：

```
xfsgo chain gethead
```

### 区块查询

最基础的功能是通过指定高度查询对应的区块数据：

```
xfsgo chain getblockbynum <number>
```

当然也可以指定区块的唯一 HASH 值查询具体区块数据：

```
xfsgo chain getblockbyhash <hash>
```

### 交易查询

您可以使用 `gettxbyhash` 命令通过指定交易的唯一 HASH 值查询已经被本矿工或者其他节点矿工封装的交易信息：

```
xfsgo chain gettxbyhash <hash>
```

### 回执查询

当交易被执行必然会产生回执信息，用以附加执行结果。你可以使用 `getreceiptbytxhash` 查询指定交易 HASH 值的具体回执信息

```
xfsgo chain getreceiptbytxhash <hash>
```
