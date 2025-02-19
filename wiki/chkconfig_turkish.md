# [Linux] C Shell (csh) chkconfig Kullanımı: Servislerin yönetimi

## Genel Bakış
`chkconfig` komutu, Linux sistemlerinde hizmetlerin (servislerin) yönetimi için kullanılır. Bu komut, sistem başlangıcında hangi hizmetlerin otomatik olarak başlatılacağını ve durdurulacağını ayarlamak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
chkconfig [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `--list`: Tüm hizmetlerin durumunu listeler.
- `--add`: Yeni bir hizmet ekler.
- `--del`: Mevcut bir hizmeti kaldırır.
- `--level`: Belirli bir çalışma seviyesinde hizmetleri ayarlamak için kullanılır.

## Yaygın Örnekler
Aşağıda `chkconfig` komutunun bazı pratik kullanım örnekleri verilmiştir:

### Tüm Hizmetlerin Durumunu Listeleme
```bash
chkconfig --list
```

### Yeni Bir Hizmet Ekleme
```bash
chkconfig --add myservice
```

### Bir Hizmeti Kaldırma
```bash
chkconfig --del myservice
```

### Belirli Bir Çalışma Seviyesinde Hizmeti Ayarlama
```bash
chkconfig myservice on --level 234
```

## İpuçları
- Hizmetlerin durumunu kontrol etmeden önce, sisteminizde hangi hizmetlerin mevcut olduğunu bilmek önemlidir.
- `chkconfig` komutunu kullanmadan önce, kök (root) kullanıcı olarak oturum açtığınızdan emin olun.
- Hizmetlerin otomatik başlatılmasını ayarlarken, yalnızca gerekli olanları etkinleştirin; bu, sistem kaynaklarınızı daha verimli kullanmanıza yardımcı olur.