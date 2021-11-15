# CHAIN Subcommand

### Usage <a href="yong-fa" id="yong-fa"></a>

```
xfsgo chain [options] <sub-command>
```

### Commands <a href="zi-ming-ling-lie-biao" id="zi-ming-ling-lie-biao"></a>

*   **gethead**

    Obtain the latest block information in the local chain data
*   **getblockbynum \<number>**

    Get block information of specified height
*   **getblockbyhash \<hash>**

    Get the block information of the specified hash
*   **gettxbyhash \<hash>**

    Get the transaction information of the specified hash
*   **gettxsbyblockhash \<hash>**

    Get all transaction sets contained in the hash of the specified block
*   **gettxsbyblocknum \<number>**

    Get all transaction sets contained in the specified block height
*   **getreceiptbytxhash \<hash>**

    Query receipt information of specified transaction hash
