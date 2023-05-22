<h1 align="center"> Ziesha Network | Deruny Testnet
  
## Ziesha Network'ün Ödüllü Node Testini kuruyoruz. Sağ üstten yıldız verip forklamayı unutmayalım. Sorularınız olursa: <a href="https://t.me/CoinHuntersTR/34102" target="_blank" rel="Coin Hunters TR" >Coin Hunters TR</a>

![1500x500](https://github.com/CoinHuntersTR/Ziesha-Network-Deruny-Testnet/assets/111747226/f29f20e1-2ccc-4edb-aa06-c4a2b38d4522)

## Sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Deruny  | 2          | 2         | 20  |
  
  
  
### Ziesha Network'ün;
  * [Github](https://github.com/ziesha-network), [Twitter](https://twitter.com/ZieshaNetwork), [Telegram](https://twitter.com/ZieshaNetwork) hesaplarını takip ettiğinizden emin olun.
  * [Discord](https://discord.gg/h4WCFZN27y) kanalına girip Deruny-Testnet rolü aldığınızdan emin olun. #role-selection kanalında mevcut
  

# Kurulum

```
sudo apt-get update && sudo apt-get upgrade -y
```

```
sudo apt install -y build-essential libssl-dev cmake
```
```
apt install git
```

```
apt install screen
```

* rustup'u kurduğunuzda 1-2-3 seçenekleri gelecek ve 1'i seçip enterleyin.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

```
git clone https://github.com/ziesha-network/bazuka
source "$HOME/.cargo/env"
```

```
cd bazuka
```
* cargo yüklemesi biraz uzun dakika sürebilir.
  
 ```
cargo install --path .
```
## Node Başlatma

* bazuka init komutunu girerken eğer daha önce cüzdan oluşturduysanız ve 12 kelimeniz varsa aşağıdaki komutu kullanabilirsiniz. IPADRESİNİZİ girmeyi unutmayın!
 ```
bazuka init --external IPADRESİNİZİ:8765 --bootstrap 31.210.53.186:8765 --mnemonic "gizli kelimelerin"
``` 
* Eğer 12 kelimeniz yoksa komutu direkt girdiğinizde size 12 kelime verecek onu saklayın. Veya [buradan](http://ziesha.network/zeejs/) oluşturabilirsiniz. Cüzdanınızı oluşturduktan sonra yukarıdaki komutu kullanabilirsiniz.

  ## Node Çalıştırma 

* Tırnak içersine discord adınızı girin. örnek "CoinHunters#6986"
```
screen -S ziesha
``` 
```
bazuka node start --discord-handle "Coinhunters#6986"
``` 
## Faydalı Komutlar

Node'umuzu ziesha adlı screen içersinde çalıştırdık:

* Node çalıştıktan sonra screen'den çıkmak için CTRL A D tuşlarına basıyoruz.
* Tekrar bu screen içersine girmek için screen -r ziesha komutunu giriyoruz.
* Eğer bu komut ile screen içersine giremezseniz screen -d -r ziesha 'yı kullanabilirsiniz.
* Screen'i silmek için screen -XS screen adı quit ve tüm screenleri silmek için pkill screen.
* Yeni screen açmak için screen -S screen adı
### Güncelleme komutu:
```
cd bazuka
git pull origin master
cargo update
cargo install --path .
screen -r ziesha
```
Bu komut her güncelleme için geçerli değildir, lütfen güncellemeler için #deruny-testnet kanalını takip edin.
 * Node güncellendikten sonra screen'e giriyoruz. CTRL C tuşlarıyla durdurup aşağıdaki kodla tekrar çalıştırıyoruz.
```
bazuka node start --discord-handle "Coinhunters#6986"
```
  
