# 钱包管理

xfsgo 程序内置了轻量级钱包服务，当守护进程启动时将会创建一个默认钱包账户。

您可以通过以下命令查看您的钱包账户列表:

```
xfsgo wallet list
```

### 创建交易账户

使用以下命令创建交易账户地址

```
xfsgo wallet new
```

### 设置默认地址

在程序运行过程中，您的一些操作将会直接使用默认地址，例如：挖矿、转账等。

您可以使用以下命令查看当前的默认地址

```
xfsgo wallet getdef
```

通过以下命令设置一个已知的地址作为默认地址

```
xfsgo wallet setdef <address>
```

### 发送交易

使用 `transfer` 命令发起一笔转账交易

```
xfsgo wallet transfer <to> <val>
```

以上命令将会使用默认地址发起指定数量的转账交易

要从指定的账户地址发起转账交易，使用以下命令

```
xfsgo wallet transfer <from> <to> <val>
```

更多的高级选项可以使用 `help` 选项查看帮助文档

### 备份以及导入

使用 `export `命令备份导出指定账户地址的私钥文件

```
xfsgo wallet export <address>
```

你可以通过以下命令导入备份的钱包地址

```
xfsgo wallet import <key>
```
