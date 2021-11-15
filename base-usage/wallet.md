# Wallet

XFSGO program has built-in lightweight wallet service. When the daemon starts, a default wallet account will be created.

You can view your wallet account list through the following command:

```
xfsgo wallet list
```

### Create Account

Create an account address using the following command:

```
xfsgo wallet new
```

### Default address

During the running of the program, some of your operations will directly use the default address, such as mining, transfer, etc.

You can use the following command to view the current default address

```
xfsgo wallet getdef
```

### Transfer transaction

Use the `transfer` command to initiate a transfer transaction

```
xfsgo wallet transfer <to> <val>
```

The above command will initiate the specified number of transfer transactions using the default address

To initiate a transfer transaction from the specified account address, use the following command

```
xfsgo wallet transfer <from> <to> <val>
```

For more advanced options, you can use the `help` option to view the help document

### Export and import

Use the `export` command to back up and export the private key file of the specified account address

```
xfsgo wallet export <address>
```

You can import the backup wallet address through the following command

```
xfsgo wallet import <key>
```
