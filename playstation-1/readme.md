# Clan Network PlayStation-1 Testnet Instructions (2/2): Prepare Node

## Details

**cland version**
`v1.0.4-alpha`

**Genesis file**

```
https://github.com/ClanNetwork/testnets/playstation-1/genesis.json
```

**Genesis sha256**

```
00df7ac7b9477597cbe5d551661190013173f2ec1985fe91f7db70c3af011d42
```

**Persistent Peers**

```
persistent_peers = "43de6c2ae93262a7369f2134c19cc87109c41006@34.73.151.40:26656,c8cf12593970f5762019f0742f911df31fc2c018@34.138.179.136:26656"
```

**Seed nodes**

N/A
## Overview

Thank you for submitting a gentx! This guide will provide instructions on getting ready for the testnet.

**The Chain Genesis Time is on 17:00 UTC on April 28, 2022**

Please have your validator up and ready by this time, and be available for further instructions if necessary
at that time.

The primary point of communication for the genesis process will be the #validators. Right now only white-listed validators can participate.
channel on the [Clan's Discord](http://discord.gg/9m4JBfD3bh).
## Instructions

This guide assumes that you have completed the [Submit Gentx part](https://github.com/ClanNetwork/testnets/blob/main/playstation-1/submit-gentx.md).
You should be running on a machine that meets the hardware requirements specified in Part 1 with Go installed. We are assuming you already have a daemon home (`$HOME/.clan`) setup.

These examples are written targeting an Ubuntu 20.04 system. Relevant changes to commands should be made depending on the OS/architecture you are running on.

Prerequisites:
You will need `jq` and for some optional parts `make` and `git`
installation:

```sh
sudo apt install build-essential jq -y

sudo apt install git
```
### 1. Update cland to v1.0.4-alpha

Please update to the `v1.0.4-alpha` tag and rebuild your binaries.

There are 2 options available:

- [Download binary from github](#option-1-download-binary-from-github)
- [Build from source](#option-2-build-from-source)

#### Option 1: Download binary from github

1. Download the binary for your platform: [releases](https://github.com/ClanNetwork/clan-network/releases/tag/v1.0.4-alpha).
2. Copy it to a location in your PATH, i.e: `/usr/local/bin` or `$HOME/bin`.

```sh
wget https://github.com/ClanNetwork/clan-network/releases/download/v1.0.4-alpha/clan-network_v1.0.4-alpha_linux_amd64.tar.gz
sudo tar -C /usr/local/bin -zxvf clan-network_v1.0.4-alpha_linux_amd64.tar.gz
```
#### Option 2: Build from source

Requires [Go version v1.18+](https://golang.org/doc/install)

```sh
# 1. Download the archive

wget https://go.dev/dl/go1.18.1.linux-amd64.tar.gz

# Optional: remove previous /go files:

sudo rm -rf /usr/local/go

# 2. Unpack:

sudo tar -C /usr/local -xzf go1.18.1.linux-amd64.tar.gz

# 3. Add the path to the go-binary to your system path:
# (for this to persist, add this line to your ~/.profile or ~/.bashrc or  ~/.zshrc)

export PATH=$PATH:/usr/local/go/bin

# 4. Verify your installation:

go version

# go version go1.18.1 linux/amd64
