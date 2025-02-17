# [Linux] Bash sysctl Kullanımı: Çekirdek parametrelerini ayarlama

## Overview
`sysctl` komutu, Linux çekirdeği ve sistem ayarlarını dinamik olarak görüntülemek ve değiştirmek için kullanılır. Bu komut, sistem performansını optimize etmek ve belirli özellikleri etkinleştirmek veya devre dışı bırakmak için önemli bir araçtır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
sysctl [options] [arguments]
```

## Common Options
- `-a`: Tüm çekirdek parametrelerini ve değerlerini listele.
- `-n`: Sadece belirtilen parametrenin değerini göster.
- `-w`: Belirtilen parametreyi yeni bir değerle ayarla.
- `-p`: Belirtilen dosyadan parametreleri yükle.

## Common Examples
Aşağıda `sysctl` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Tüm çekirdek parametrelerini listeleme:
   ```bash
   sysctl -a
   ```

2. Belirli bir parametrenin değerini görüntüleme (örneğin, `vm.swappiness`):
   ```bash
   sysctl -n vm.swappiness
   ```

3. Bir parametreyi yeni bir değerle ayarlama (örneğin, `vm.swappiness` değerini 10 olarak ayarlama):
   ```bash
   sysctl -w vm.swappiness=10
   ```

4. Bir dosyadan parametreleri yükleme (örneğin, `/etc/sysctl.conf`):
   ```bash
   sysctl -p
   ```

## Tips
- `sysctl` komutunu kullanmadan önce, değişikliklerin sistem üzerindeki etkilerini anlamak önemlidir.
- Değişikliklerin kalıcı olması için, ayarları `/etc/sysctl.conf` dosyasına eklemeyi unutmayın.
- Sisteminizdeki çekirdek parametrelerini düzenli olarak kontrol etmek, performans sorunlarını önlemeye yardımcı olabilir.