# [Linux] C Shell (csh) xargs Kullanımı: Komut çıktısını argüman olarak kullanma

## Genel Bakış
`xargs` komutu, standart girişten aldığı verileri alarak bunları bir komutun argümanları olarak kullanır. Bu, özellikle uzun komut dizilerini veya çok sayıda dosya ismini işlemek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
xargs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n`: Her seferinde kaç argüman kullanılacağını belirtir.
- `-d`: Girdi ayırıcı karakterini belirtir.
- `-p`: Her komut çalışmadan önce onay ister.
- `-0`: Null karakter ile ayrılmış girdileri işler (genellikle `find` ile birlikte kullanılır).

## Yaygın Örnekler
1. **Dosya isimlerini silme**:
   Belirli bir uzantıya sahip dosyaları bulup silmek için:
   ```bash
   find . -name "*.tmp" | xargs rm
   ```

2. **Dosya içeriğini sayma**:
   Belirli bir dizindeki tüm `.txt` dosyalarının satır sayısını bulmak için:
   ```bash
   ls *.txt | xargs wc -l
   ```

3. **Girdi ayırıcı olarak boşluk kullanma**:
   Boşluk ile ayrılmış girdileri işlemek için:
   ```bash
   echo "file1 file2 file3" | xargs -n 1 echo
   ```

4. **Null karakter ile ayrılmış girdilerle çalışma**:
   `find` komutuyla birlikte kullanarak dosyaları güvenli bir şekilde silmek için:
   ```bash
   find . -type f -print0 | xargs -0 rm
   ```

## İpuçları
- `xargs` kullanırken, çok sayıda dosya ile çalışıyorsanız `-n` seçeneği ile her seferinde kaç dosya işleneceğini kontrol edebilirsiniz.
- Girdi ayırıcı karakterlerini değiştirmek için `-d` seçeneğini kullanarak özel karakterler belirleyebilirsiniz.
- Komutların çalışmadan önce onay almasını istiyorsanız `-p` seçeneğini kullanabilirsiniz; bu, yanlışlıkla istenmeyen işlemler yapmanızı önler.