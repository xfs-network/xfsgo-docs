# Installation

### Before you start

In order to use XFS-Network effectively, you need to know what it is and understand some of its fundamental concepts. So before you start using XFS-Network in earnest, we highly recommend you read [What is XFS?](https://docs.xfs.tech/#overview)

XFSGO is the official implementation version of XFS-Network, you can view this repositories:&#x20;

{% embed url="https://github.com/xfs-network/xfsgo" %}

XFSGO can be installed differently, depending on the operating system. In order to create a new network node, you will need to install XFSGO according to these instructions. Note that there may be other ways to install XFSGO in addition to those described on that page, since it’s nearly impossible to keep track of all the package managers out there.

### Building from Sources

#### Prerequisites

Install some necessary system dependencies. On Ubuntu/Debian:

```
sudo apt-get install build-essential
```

To build from source, Go 1.16.4 or above must be installed on the system. This guide doesn’t cover how to install Go itself, for details read the Go installation instructions and grab any needed bundles from the Go [download page](https://golang.org/doc/install) . Via Linux system for example: &#x20;

```bash
curl -L https://golang.org/dl/go1.17.3.linux-amd64.tar.gz | tar -xz -C /usr/local
```

Set the Environment variable PATH to point to Go:

```
echo 'export PATH=/usr/local/go/bin:$PATH' >> ~/.bashrc && source ~/.bashrc
```

#### Build and install XFSGO

Clone the repository to a directory of your choosing :

```bash
git clone https://github.com/xfs-network/xfsgo.git
```

Run make command to compile from source:

```bash
cd xfsgo && make && make install
```

This will put `xfsgo` in `/usr/local/bin`.  You should now have `xfsgo` installed,  run `xfsgo version` to check your version:

```bash
xfsgo version
```







