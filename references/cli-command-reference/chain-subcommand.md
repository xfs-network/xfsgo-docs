# CHAIN 子命令

### 用法

```
xfsgo chain [options] <sub-command>
```

### 子命令列表

*   **gethead**

    获取本地链数据最新区块信息
*   **getblockbynum \<number>**

    查询指定高度的区块信息
*   **getblockbyhash \<hash>**

    查询指定 HASH 值的区块信息
*   **gettxbyhash \<hash>**

    查询指定 HASH 值的交易信息
*   **gettxsbyblockhash \<hash>**

    查询指定区块 HASH 值包含的所有交易集合
*   **gettxsbyblocknum \<number>**

    查询指定区块高度包含的所有交易集合
*   **getreceiptbytxhash \<hash>**

    查询指定交易 HASH 的回执信息
