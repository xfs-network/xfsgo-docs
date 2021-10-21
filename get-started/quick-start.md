# Quick start

### Start daemon and sync the chain

The `xfsgo` application runs as a daemon and a client to control and interact with that daemon. A daemon is a long-running program that is usually run in the background.

You can start the daemon with the following command:

```
xfsgo daemon
```

If you run it for the first time, xfsgo will initially set the data directory to `~/.xfsgo` by default. At the same time, xfsgo will start the P2P network service and connect to the default bootstrap node for network data synchronization.

### Interact with the daemon

The xfsgo command allows you to interact with a running xfsgo daemon. xfsgo comes with built-in CLI documentation. You can view with the following command:

```
xfsgo -h
```

