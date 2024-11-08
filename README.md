# Clan Network - Testnet

Clan Network için test ağları deposu

# Minimum sistem gereksinimleri :
```
4GB RAM
50GB+ disk
2 vcpu
```
# Node kontrol ve stake işlemi için linkler:
```
https://secretnodes.com/clan/chains/playstation-2
https://stake-testnet.clan.network/
```

# Gerekli paketleri güncelleyip varsa mevcut yeni sürümlerine güncelleriz:

```
sudo apt-get update && sudo apt upgrade -y
```
# Go kurulumu:

```
wget https://go.dev/dl/go1.18.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.18.linux-amd64.tar.gz

cat <<EOF >> ~/.profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF


source ~/.profile
```
