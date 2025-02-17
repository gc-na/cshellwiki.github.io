# [Linux] Bash xargs Kullanımı: Komutları birleştirerek çalıştırma

## Genel Bakış
`xargs` komutu, standart girişten aldığı verileri alarak bu verileri bir komutun argümanları olarak kullanır. Bu, özellikle uzun veya çok sayıda argüman gerektiren komutları çalıştırmak için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
xargs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n`: Her seferinde kaç argüman kullanılacağını belirtir.
- `-d`: Argümanların ayrılacağı karakteri tanımlar.
- `-p`: Her komut çalıştırılmadan önce onay ister.
- `-0`: Null karakter (`\0`) ile ayrılmış girişleri işler; bu, dosya adlarında boşluk olan durumlar için kullanışlıdır.

## Yaygın Örnekler

### 1. Dosya Silme
Belirli bir uzantıya sahip dosyaları silmek için kullanılabilir:

```bash
find . -name "*.tmp" | xargs rm
```

### 2. Dosya İçeriğini Görüntüleme
Birden fazla dosyanın içeriğini görüntülemek için:

```bash
ls *.txt | xargs cat
```

### 3. Belirli Sayıda Argüman ile Komut Çalıştırma
Her seferinde yalnızca 2 dosya ile `echo` komutunu çalıştırmak:

```bash
ls | xargs -n 2 echo
```

### 4. Null Karakter ile Ayrılmış Girişler
Boşluk içeren dosya adları için:

```bash
find . -name "*.jpg" -print0 | xargs -0 rm
```

## İpuçları
- `xargs` kullanırken, girdi verilerinin boyutunu göz önünde bulundurun; çok fazla argüman, komutun başarısız olmasına neden olabilir.
- `-p` seçeneği ile komutları çalıştırmadan önce onay alarak yanlışlıkla istenmeyen işlemler yapmaktan kaçınabilirsiniz.
- `-0` seçeneği ile birlikte kullanarak, dosya adlarında boşluk veya özel karakterler olan durumlarda güvenli bir şekilde çalışabilirsiniz.