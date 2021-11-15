# Miner

Miners are participants on the network who perform the work needed to advance the blockchain and maintain its effectiveness. In order to provide these services, miners are paid in local cryptocurrency.

Mining is the process of creating new blocks. New blocks are always created in xfsgo network, but these blocks need to be protected by workload proof so that other nodes can accept them. Mining is to create the value of these workloads.

Before starting mining, always ensure that your blockchain is fully synchronized with the network chain, otherwise you will not be able to mine on the correct chain, and your blockawards will be worthless. You can use the following command to view the progress of the current synchronization:

```
xfsgo chain syncstatus
```

### Start worker

When the chain data synchronization is completed, use the `start` command to start the miner and start work

```
xfsgo miner start
```

By default, the above command will start an appropriate number of worker threads based on the maximum number of threads of the local computer's CPU

To customize the number of worker threads at startup, you can specify the workers parameter

```
xfsgo miner start --workers <number>
```

You can also use the `setworkers` command after startup to dynamically adjust the number of working threads running

```
xfsgo miner setworkers <number>
```

### Check running status

Use the `status` command to view the working status of the current miner and some reference indicators:

```
xfsgo miner status
```
