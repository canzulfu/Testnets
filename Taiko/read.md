Taiko
Donanım
Hetzner'i 3$ sunucuyu kullandım. Link

2 CPU 
4 GB RAM 
50 GB SSD 
Kurulum
# Komutları tek tek girelim.
sudo apt update 
sudo apt upgrade
apt install docker-compose
apt install git
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin

# Repoyu klonlayıp dizine girelim.
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node

#Ayrı screende çalıştıracağız:
screen -S taiko
Dikkat edilmesi gereken nokta
Alchemy hesabımdan taiko için bir dApp oluşturdum.

Bu dApp, Ethereum - Sepolia zinciri olacak.

image

Daha sonra View key kısmından key bilgilerimi aldım:

image

Altta ki komutlar ile .env içine girdim.

cd simple-taiko-node
cp .env.sample .env
nano .env
L1_ENDPOINT_HTTP= Bu kısıma Alchemyden aldığınız HTTPS adresini yazıyorsunuz

L1_ENDPOINT_WS= Bu kısıma Alchemyden aldığınız WSS adresini yazıyorsunuz

L1_PROVER_PRIVATE_KEY= Bu kısıma Metamask Private keyinizi yapıştırıyorsunuz

CTRL X Y ile çıkıyoruz.

image

Node'u çalıştırma
Faucet Linki https://sepoliafaucet.com/

# Node'u çalıştırın
docker compose up
image
