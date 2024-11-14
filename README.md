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
Bu komutu girdiğiniz zaman aşağıda ki çıktıyı alırsınız, komut:

```
go version
```
Alacağınız çıktı: 

```
go version go1.18 linux/amd64
```
# Clan network dosyalarını indirme:

```
wget https://github.com/ClanNetwork/clan-network/releases/download/v1.0.4-alpha/clan-network_v1.0.4-alpha_linux_amd64.tar.gz
sudo tar -C /usr/local/bin -zxvf clan-network_v1.0.4-alpha_linux_amd64.tar.gz

git clone https://github.com/ClanNetwork/clan-network
cd clan-network
git fetch origin --tags
git checkout v1.0.4-alpha

make install
```
Gerekli düzenlemeleri yapıyoruz: chainid - peer - monikername

```
CHAIN_ID=playstation-2
```
# TEST yazan kısmı kendinize göre düzenleyin, örnek MONIKER_NAME="RUES" :

```
MONIKER_NAME="TEST"
```
```
CHAIN_REPO="https://raw.githubusercontent.com/ClanNetwork/testnets/main/$CHAIN_ID" && \
export PEERS="$(curl -s "$CHAIN_REPO/persistent-peers.txt")"
```
# Bu komuttan sonra aşşağıdaki gibi bir çıktı almalısınız, komut:
```
echo $PEERS
```
