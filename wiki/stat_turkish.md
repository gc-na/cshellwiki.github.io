# [Linux] C Shell (csh) stat Kullanımı: Dosya bilgilerini görüntüleme

## Overview
`stat` komutu, dosyaların ve dizinlerin detaylı bilgilerini görüntülemek için kullanılır. Bu bilgiler arasında dosya boyutu, oluşturulma tarihi, son erişim tarihi ve izinler gibi veriler bulunur.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
stat [options] [arguments]
```

## Common Options
- `-c` : Özelleştirilmiş çıktı formatı belirtir.
- `-f` : Dosya sistemine özgü bilgileri görüntüler.
- `-L` : Sembolik bağlantıların hedef dosyalarının bilgilerini gösterir.
- `--help` : Komut hakkında yardım bilgisi gösterir.

## Common Examples
Aşağıda `stat` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosyanın bilgilerini görüntülemek:
   ```bash
   stat dosya.txt
   ```

2. Bir dizinin bilgilerini görüntülemek:
   ```bash
   stat /home/kullanici
   ```

3. Özelleştirilmiş çıktı formatı ile dosya bilgilerini görüntülemek:
   ```bash
   stat -c '%s %y' dosya.txt
   ```

4. Sembolik bağlantının hedef dosyasının bilgilerini görüntülemek:
   ```bash
   stat -L link.txt
   ```

## Tips
- Dosya bilgilerini hızlıca kontrol etmek için `stat` komutunu sıkça kullanın.
- Özelleştirilmiş formatlar kullanarak yalnızca gerekli bilgileri görüntüleyebilirsiniz.
- Sembolik bağlantılarla çalışırken `-L` seçeneğini kullanmayı unutmayın, aksi takdirde bağlantının kendisi hakkında bilgi alırsınız.