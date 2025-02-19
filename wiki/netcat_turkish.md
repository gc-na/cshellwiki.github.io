# [Linux] C Shell (csh) netcat Kullanımı: Ağ bağlantıları kurma ve veri iletme aracı

## Genel Bakış
Netcat, ağ bağlantıları kurmak ve veri iletmek için kullanılan bir araçtır. TCP ve UDP protokollerini destekler ve genellikle ağ sorunlarını giderme, veri transferi ve güvenlik testleri için kullanılır.

## Kullanım
Netcat komutunun temel sözdizimi aşağıdaki gibidir:

```bash
netcat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Dinleyici modunu etkinleştirir.
- `-p`: Belirtilen portu kullanır.
- `-u`: UDP protokolünü kullanır.
- `-v`: Ayrıntılı çıktı sağlar.
- `-z`: Port taraması yapar, bağlantı kurmadan kontrol eder.

## Yaygın Örnekler
Aşağıda netcat komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Bir TCP sunucusu başlatma**:
   ```bash
   netcat -l -p 1234
   ```

2. **Bir TCP istemcisi olarak bağlanma**:
   ```bash
   netcat 192.168.1.1 1234
   ```

3. **Bir dosyayı bir sunucuya gönderme**:
   ```bash
   netcat -l -p 1234 > gelen_dosya.txt
   ```
   Başka bir terminalde:
   ```bash
   netcat 192.168.1.1 1234 < giden_dosya.txt
   ```

4. **Port taraması yapma**:
   ```bash
   netcat -z -v 192.168.1.1 1-1000
   ```

## İpuçları
- Netcat'i güvenlik testleri için kullanırken dikkatli olun; izinsiz erişim yasadışıdır.
- Dinleyici modunda çalışırken, dinlediğiniz portun açık olduğundan emin olun.
- Veri iletiminde, verilerin bütünlüğünü sağlamak için şifreleme yöntemlerini düşünün.