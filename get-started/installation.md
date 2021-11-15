# 安装指引

### 引言

为了有效地使用 XFS 网络，您需要了解它是什么，并理解它的一些基本概念。因此，在您开始认真使用XFS网络之前，我们强烈建议您阅读 XFSGO 介绍。

XFSG O 是 XFS Network 的官方实现版本，您可以查看以下存储库：

{% embed url="https://github.com/xfs-network/xfsgo.git" %}

不同的操作系统环境下 XFSGO 的安装方式可能有所不同。为了创建新的网络节点，您需要按照以下说明安装 XFSGO。请注意，除了该页面上描述的方法之外，可能还有其他方法安装 XFSGO，因为几乎不可能跟踪所有的包管理器。

### 从源码中构建

#### 前提条件

在编译源码之前需要安装一些必要的系统依赖项，下面列举了一些常见操作系统的安装方式

* Debian/Ubuntu:

```bash
sudo apt-get install build-essential
```

XFSGO 使用 Go 语言作为基础开发语言，在编译之前必须在系统上安装 Go 1.16.4 或更高版本。

{% hint style="info" %}
本指南不包括如何安装 Go 环境，有关详细信息，请阅读 Go 安装说明并从 [Go 下载页面](https://golang.org/doc/install) 获取所需的捆绑包。
{% endhint %}

例如，在 Linux 系统中安装：

```bash
curl -L https://golang.org/dl/go1.16.4.linux-amd64.tar.gz | tar -xz -C /usr/local
```

配置 GO 系统环境变量

```bash
echo 'export PATH=/usr/local/go/bin:$PATH' >> ~/.bashrc && source ~/.bashrc
```

#### 开始编译安装

从 Git 仓库中下载源码

```bash
git clone https://github.com/xfs-network/xfsgo.git
```

运行以下命令，快速启动编译并且安装

```bash
cd xfsgo && make && make install
```

如果以上步骤执行成功后，`xfsgo `程序将会被安装至 `/usr/local/bin` 目录。

在 Windows 系统环境中编译安装，建议切换到工程目录，并且使用 `go install` 命令直接编译安装

（在此之前请先检查你的 GO 环境配置有效且能正常工作）使用 `PowerShell` 执行以下命令：

```
cd xfsgo
go install ./cmd/xfsgo/...
```

完成 `go install` 操作后，你可以在 `$GOPATH/bin` 目录中查看到编译的二进制程序，你可以设置系统 PATH 变量，使得该目录在全局有效。

现在可以使用以下命令查看并检查已安装 `xfsgo` 程序的版本

```bash
xfsgo version
```
