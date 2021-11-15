# MINER Subcommand

### Usage

```
xfsgo miner [options] <sub-command>
```

### Commands

*   **start \[--workers \<num>]**

    Start the worker thread and start encapsulating the block. Use the workers option to specify the number of worker threads to start
*   **status**

    Get service status and parameter indicators
*   **setworkers \<number>**

    Set the number of worker threads, which can be dynamically adjusted during operation
*   **setgasprice \<value>**

    Set the minimum transaction burning fee price accepted by the miner
*   **stop**

    Stop all worker threads
