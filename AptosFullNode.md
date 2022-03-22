**Aşamalar**

- **Proje bir devnet başlattı.**

- **Ödüllü test ağı 2022'nin ikinci çeyreği için duyuruldu**

- **Mainnet, 2022'nin 3. Çeyreği için planlandı**


**Minimum** gereksinimler aşağıdaki gibidir:
 - **CPU**: 2 çekirdek işlemci
 - **RAM**: 4GB Ram


**Sıfırdan Kurulum İçin Yapılması Gerekenler**

- **Screen ile bir sayfa oluşturuyoruz**
- 
```
screen -S Anasayfa
```

**FullNode Kurulumu ve Key Oluşturma Scripti**

```
wget -q -O aptos.sh https://api.zvalid.com/aptos.sh && chmod +x aptos.sh && sudo /bin/bash aptos.sh
```

**Senkronizasyon Durumunu Kontrol Etme**

- **CTRL A-C ile yeni sayfa açtıktan sonra**

```
curl 127.0.0.1:9101/metrics 2> /dev/null | grep aptos_state_sync_version | grep type
```

**Logları Görüntüleme**

- **CTRL A-C ile yeni sayfa açtıktan sonra**

```
docker logs -f aptos-fullnode-1 --tail 5000
```

**FirstTransaction Adımı**

- **CTRL A-C ile yeni sayfa açtıktan sonra**

```
apt install python3-pip
```

```
wget https://raw.githubusercontent.com/aptos-labs/aptos-core/main/developer-docs-site/static/examples/python/first_transaction.py
```

```
python3 first_transaction.py
```

- **Sayfalar arası geçisi CTRL A-P ile yapabilirsiniz**


**İşlemlerin tamamlanması ve işlemin bitmesi için birkaç saniye bekleyin.**
  
  

**End**

- **https://t.me/aptos_tr**

- **https://t.me/testnetrun**

- **https://testnet.run/**

- **https://stake.testnet.run/**

- **https://twitter.com/testnetrun**




