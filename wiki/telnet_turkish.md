# [Linux] Bash telnet Kullanımı: Uzak sunuculara bağlantı kurma

## Genel Bakış
Telnet komutu, kullanıcıların uzak bir sunucuya veya cihaza metin tabanlı bir iletişim kurarak bağlanmasını sağlar. Genellikle, ağ bağlantılarını test etmek veya uzak sistemlerle etkileşimde bulunmak için kullanılır.

## Kullanım
Telnet komutunun temel sözdizimi aşağıdaki gibidir:

```bash
telnet [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l [kullanıcı]`: Belirtilen kullanıcı adı ile oturum açar.
- `-d`: Hata ayıklama modunu etkinleştirir.
- `-n [dosya]`: İletişim günlüklerini belirtilen dosyaya kaydeder.

## Yaygın Örnekler
Aşağıda telnet komutunun bazı pratik örnekleri verilmiştir:

### 1. Bir sunucuya bağlanma
```bash
telnet example.com 80
```
Bu komut, `example.com` adresindeki 80 numaralı porta bağlanır.

### 2. Hata ayıklama modunu etkinleştirme
```bash
telnet -d example.com 80
```
Bu komut, `example.com` adresine bağlanırken hata ayıklama modunu etkinleştirir.

### 3. Belirli bir kullanıcı adı ile oturum açma
```bash
telnet -l myuser example.com
```
Bu komut, `example.com` adresine `myuser` kullanıcı adı ile bağlanır.

## İpuçları
- Telnet, şifreli bir bağlantı sağlamaz. Hassas bilgileri iletmek için SSH kullanmayı tercih edin.
- Bağlantı sorunlarını gidermek için telnet komutunu kullanarak belirli bir portun açık olup olmadığını kontrol edebilirsiniz.
- Telnet oturumunu kapatmak için `Ctrl + ]` tuşlarına basarak telnet komut istemine geçebilir ve ardından `quit` yazarak çıkabilirsiniz.