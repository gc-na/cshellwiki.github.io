# [Linux] Bash uname Kullanımı: Sistem bilgilerini görüntüleme

## Genel Bakış
`uname` komutu, işletim sistemi hakkında bilgi almak için kullanılan bir Bash komutudur. Bu komut, sistemin çekirdek adı, sürüm numarası, mimarisi gibi bilgileri görüntülemenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
uname [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bilgileri bir arada gösterir.
- `-s`: Çekirdek adını gösterir.
- `-n`: Ağ ana bilgisayar adını gösterir.
- `-r`: Çekirdek sürümünü gösterir.
- `-v`: Çekirdek sürüm bilgilerini gösterir.
- `-m`: Makine mimarisini gösterir.
- `-p`: İşlemci türünü gösterir.
- `-i`: Donanım platformunu gösterir.
- `-o`: İşletim sistemi adını gösterir.

## Yaygın Örnekler
Aşağıda `uname` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Tüm sistem bilgilerini görüntüleme:**
   ```bash
   uname -a
   ```

2. **Çekirdek adını görüntüleme:**
   ```bash
   uname -s
   ```

3. **Çekirdek sürümünü görüntüleme:**
   ```bash
   uname -r
   ```

4. **Makine mimarisini görüntüleme:**
   ```bash
   uname -m
   ```

5. **Ağ ana bilgisayar adını görüntüleme:**
   ```bash
   uname -n
   ```

## İpuçları
- `uname -a` komutunu kullanarak sistem hakkında kapsamlı bilgi alabilirsiniz.
- Sadece belirli bir bilgiye ihtiyaç duyuyorsanız, ilgili seçeneği kullanarak daha az bilgi görüntüleyebilirsiniz.
- `uname` komutunu bir betik içinde kullanarak sistem bilgilerini otomatik olarak alabilir ve işleyebilirsiniz.