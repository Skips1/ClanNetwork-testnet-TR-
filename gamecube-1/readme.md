# Clan Network's gamecube-1 Testnet Instructions

gamecube-1 testnet purpose is to serve as a development testnet, mainly to test the airdrop modules

## Minimum hardware requirements

- 2x CPUs
- 4GB RAM
- 25GB+ of disk space
## Install Clan Network

### Option 1: Download binary

1. Download the binary for your platform: [releases](https://github.com/ClanNetwork/clan-network/releases/tag/latest).
2. Copy it to a location in your PATH, i.e: `/usr/local/bin` or `$HOME/bin`.

i.e:
```sh
> wget https://github.com/ClanNetwork/clan-network/releases/download/latest/clan-network_latest_linux_amd64.tar.gz
> sudo tar -C /usr/local/bin -zxvf clan-network_latest_linux_amd64.tar.gz
```
### Option 2: Build from source

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
```

```sh
mkdir -p $GOPATH/src/github.com/ClanNetwork
cd $GOPATH/src/github.com/ClanNetwork
git clone https://github.com/ClanNetwork/clan-network && cd clan-network
git fetch origin --tags
make install
```
