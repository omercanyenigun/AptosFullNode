**Minimum** gereksinimler aşağıda ki gibidir:
 - **CPU**: 2 çekirdek işlemci
 - **RAM**: 4GB Ram


```screen -S Anasayfa```
**screen ile bir sayfa oluşturuyoruz.**

```sudo apt update```

```sudo apt install ca-certificates curl gnupg lsb-release wget -y```

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg```

```echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```

```sudo apt update```

```sudo apt install docker-ce docker-ce-cli containerd.io -y```

```docker version```

**docker versiyonu 20.10.13 olarak gözüküyptsa buraya kadar hiçbir sorun yoktur.**

```mkdir -p ~/.docker/cli-plugins/```

```curl -SL https://github.com/docker/compose/releases/download/v2.2.3/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose```

```chmod +x ~/.docker/cli-plugins/docker-compose```

```sudo chown $USER /var/run/docker.sock```

```docker compose version```

**compose versiyon v2.2.3 olması gerek.**

```mkdir $HOME/aptos``` 
**bu kod ile bir dosya oluşturuyoruz. Aptos yerine başka dosya adı kullanabilirsiniz.**

```cd $HOME/aptos```
**oluşturduğumuz dosyanın içine giriyoruz.**  

```wget https://raw.githubusercontent.com/aptos-labs/aptos-core/main/docker/compose/public_full_node/docker-compose.yaml```

```wget https://raw.githubusercontent.com/aptos-labs/aptos-core/main/docker/compose/public_full_node/public_full_node.yaml```

```wget https://devnet.aptoslabs.com/genesis.blob```

```wget https://devnet.aptoslabs.com/waypoint.txt```

**gerekli dosyaları bu kodlarla indiriyoruz.**

```docker compose up -d``` 

**node başlatma**

**Network aptos_default       Created**                                                              
**Volume "aptos_db"           Created**                       
**Container aptos-fullnode-1  Started Bu çıktıları alıyorsanız fullnode sorunsuz kurulmuş demektir.**

ctrl + A-C
**yaparak yeni bir sayfa açıyoruz. 

```docker logs -f aptos-fullnode-1 --tail 5000```

**bu sayfada kodu yazarak logların akışını görebilirsiniz. **
**Sayfalar arasında ctrl + A-P ile geçiş yapabilirsiniz.**
**End**

**https://t.me/aptos_tr**
**https://t.me/testnetrun**
**https://testnet.run/**
**https://stake.testnet.run/**
**https://twitter.com/testnetrun**




