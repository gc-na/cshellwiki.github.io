# [Linux] Bash chkconfig Kullanımı: Servislerin yönetimi

## Genel Bakış
`chkconfig` komutu, Linux sistemlerinde hizmetlerin (servislerin) başlangıçta hangi seviyelerde çalışacağını yönetmek için kullanılır. Bu komut, sistem yöneticilerine, belirli hizmetlerin otomatik olarak başlatılıp başlatılmayacağını ayarlama imkanı sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
chkconfig [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `--list`: Tüm hizmetlerin durumunu listelemek için kullanılır.
- `--add`: Yeni bir hizmet eklemek için kullanılır.
- `--del`: Mevcut bir hizmeti kaldırmak için kullanılır.
- `--level`: Belirli bir çalışma seviyesinde hizmetleri ayarlamak için kullanılır.
- `on`: Hizmeti belirtilen seviyelerde etkinleştirmek için kullanılır.
- `off`: Hizmeti belirtilen seviyelerde devre dışı bırakmak için kullanılır.

## Yaygın Örnekler
Aşağıda `chkconfig` komutunun bazı pratik kullanım örnekleri verilmiştir:

1. Tüm hizmetlerin durumunu listeleme:
   ```bash
   chkconfig --list
   ```

2. Yeni bir hizmet ekleme:
   ```bash
   chkconfig --add myservice
   ```

3. Mevcut bir hizmeti kaldırma:
   ```bash
   chkconfig --del myservice
   ```

4. Belirli bir seviyede bir hizmeti etkinleştirme:
   ```bash
   chkconfig myservice on
   ```

5. Belirli bir seviyede bir hizmeti devre dışı bırakma:
   ```bash
   chkconfig myservice off
   ```

## İpuçları
- `chkconfig` komutunu kullanmadan önce, hangi hizmetlerin sisteminizde mevcut olduğunu kontrol edin.
- Hizmetlerin başlangıç seviyelerini ayarlarken dikkatli olun; yanlış ayarlar sistemin başlatılmasını etkileyebilir.
- `chkconfig` ile yapılan değişikliklerin etkili olabilmesi için, sistemin yeniden başlatılması gerekebilir.