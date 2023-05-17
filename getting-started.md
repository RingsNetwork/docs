---
description: Start from using rings-node
---

# Getting started

## Installation

You can install rings-node either from Cargo or from source.

From Cargo:

```
cargo install rings-node
```

From Source

```
git clone https://github.com/RingsNetwork/rings-node
cd rings-node
cargo build
```

### Usage

```
rings <command> [options]
```

#### Commands

* `help`: displays the usage information.
* `init`: creates a default configuration file named `config.toml` in the current directory. This file can be edited to customize the behavior of the rings-node daemon.
* `run`: runs the rings-node daemon. This command starts the daemon process, which will validate transactions, maintain the blockchain, and participate in consensus to earn rewards. By default, the daemon will use the `config.toml` file in the current directory for configuration. Use the "-c" or "--config" option to specify a custom configuration file.

#### Options

* `-c, --config <FILE>`: specifies a custom configuration file to use instead of the default `config.toml`. The configuration file is used to specify the network configuration, account settings, and other parameters that control the behavior of the rings-node daemon.
* `-h, --help`: displays the usage information.
* `-V, --version`: displays the version information for rings-node.
