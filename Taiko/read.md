<h1 align="center">Taiko Node Kurulum</h1>

<h2 align="center">Donanım</h2>

``` 2 CPU 4 GB RAM 50 GB SSD ```

<h2 align="center">Kurulum</h2>

``` Console
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
```

<h2 align="center">Dikkat edilmesi gereken nokta</h2>

>Alchemy hesabımdan taiko için bir dApp oluşturdum.

>Bu dApp, Ethereum - Sepolia zinciri olacak.

<h2 align="center">Altta ki komutlar ile .env içine girdim.</h2>

```console
cd simple-taiko-node
cp .env.sample .env
nano .env
```

>L1_ENDPOINT_HTTP= Bu kısıma Alchemyden aldığınız HTTPS adresini yazıyorsunuz

>L1_ENDPOINT_WS= Bu kısıma Alchemyden aldığınız WSS adresini yazıyorsunuz

>L1_PROVER_PRIVATE_KEY= Bu kısıma Metamask Private keyinizi yapıştırıyorsunuz

>CTRL X Y ile çıkıyoruz.


>Node'u çalıştırma
>Faucet Linki https://sepoliafaucet.com/

<h2 align="center"> Node'u çalıştırın</h2>

```console
docker compose up
```
