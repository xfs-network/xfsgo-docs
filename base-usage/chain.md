# Chain

During the operation of the node, whether it is synchronous data from the network or locally encapsulated blocks, historical block data will be generated locally. You can use the chain command to view local historical chain data. For example, you can view the latest local blocks through the following command:

```
xfsgo chain gethead
```

### Blocks

The most basic function is to query the corresponding block data through the specified height:

```
xfsgo chain getblockbynum <number>
```

You can also specify the unique hash value of the block to query the specific block data

```
xfsgo chain getblockbyhash <hash>
```

### Transactions

You can use the gettxbyhash command to query the transaction information encapsulated by this miner or other node miners by specifying the unique hash value of the transaction:

```
xfsgo chain gettxbyhash <hash>
```

### Receipts

When the transaction is executed, the receipt information will be generated to attach the execution result. You can use `getreceiptbytxhash` to query the specific receipt information of the hash value of the specified transaction

```
xfsgo chain getreceiptbytxhash <hash>
```
