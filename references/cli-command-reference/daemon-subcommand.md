# DAEMON Subcommand

### Usage

```
xfsgo daemon [--datadir <filename>] [--netid <number>]
             [--p2paddr <address>] [--rpcaddr <address>]
             [--testnet] [--bootstrap <node1,...>]
```

### Command options

*   **--datadir, -d \<filename>**

    Set the global data directory, which will be created in the system user directory by default
*   **--netid, -n \<number>**

    Set the network ID, which is not specified as the primary network by default (0)
*   **--p2paddr, -p \<addr>**

    Set the P2P node service network listening address and port. Default: 0.0.0.0:9091
*   **--rpcaddr, -r \<addr>**

    Set the RPC service network listening address and port
*   **--testnet, -t**

    Start the test network. This option overrides the netid option setting
*   **--bootstrap \<uri\[,uri...]>**

    Set the boot node. Multiple node links are separated by commas

