# Clan Network PlayStation-1 Testnet Instructions (1/2): Submit Gentx

## Minimum hardware requirements

- 2x CPUs
- 4GB RAM
- 50GB+ of disk space

### Install Clan Network
#### Download binary from github

1. Download the binary for your platform: [releases](https://github.com/ClanNetwork/clan-network/releases/tag/v1.0.0-alpha).
2. Copy it to a location in your PATH, i.e: `/usr/local/bin` or `$HOME/bin`.

```sh
> wget https://github.com/ClanNetwork/clan-network/releases/download/v1.0.0-alpha/clan-network_v1.0.0-alpha_linux_amd64.tar.gz
> sudo tar -C /usr/local/bin -zxvf clan-network_v1.0.0-alpha_linux_amd64.tar.gz
```
#### Verify installation

To verify if the installation was successful, execute the following command:

```sh
cland version --long
```

It will display the version of `cland` currently installed:

```sh
name: Clan-Network
server_name: clan-networkd
version: latest
commit: a7ee4541dbb19e55221bbb575284eeb39c462610
build_tags: ""
go: go version go1.18 linux/amd64
```
