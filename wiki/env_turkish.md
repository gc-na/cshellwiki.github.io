# [Linux] Bash env Kullanımı: Ortam Değişkenlerini Yönetme

## Genel Bakış
`env` komutu, ortam değişkenlerini görüntülemek, ayarlamak veya çalıştırmak için kullanılır. Bu komut, belirli bir ortamda bir komut çalıştırmak için ortam değişkenlerini geçici olarak değiştirmeye olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
env [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Temiz bir ortam ile başlar; mevcut ortam değişkenlerini yok sayar.
- `-u`: Belirtilen ortam değişkenini kaldırır.
- `VAR=değer`: Belirtilen ortam değişkenini geçici olarak ayarlar.

## Yaygın Örnekler
1. Ortam değişkenlerini görüntüleme:
   ```bash
   env
   ```

2. Belirli bir ortam değişkenini ayarlayarak bir komut çalıştırma:
   ```bash
   env VAR=value komut
   ```

3. Temiz bir ortamda bir komut çalıştırma:
   ```bash
   env -i komut
   ```

4. Belirli bir ortam değişkenini kaldırarak bir komut çalıştırma:
   ```bash
   env -u VAR komut
   ```

## İpuçları
- `env` komutunu, bir betik veya programın hangi ortam değişkenleri ile çalıştığını görmek için kullanabilirsiniz.
- Geçici ortam değişkenleri ayarlamak için `env` komutunu kullanarak, sistem genelindeki ayarları etkilemeden denemeler yapabilirsiniz.
- `env` komutunu, farklı ortam değişkenleri ile bir komutu test etmek için faydalı bir araç olarak değerlendirin.