# [Linux] C Shell (csh) awk Kullanımı: Metin işleme ve analiz aracı

## Genel Bakış
`awk`, metin dosyalarını işlemek ve analiz etmek için kullanılan güçlü bir programlama dilidir. Genellikle veri biçimlendirme, filtreleme ve raporlama işlemleri için tercih edilir. `awk`, belirli bir desenle eşleşen satırları bulmak ve bu satırlardaki verileri işlemek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
awk [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-F`: Girdi dosyasındaki alan ayırıcıyı belirler. Örneğin, `-F,` virgülü alan ayırıcı olarak kullanır.
- `-v`: Değişken tanımlamak için kullanılır. Örneğin, `-v var=değer` ile `var` değişkenine `değer` atanır.
- `-f`: Belirtilen bir dosyadan `awk` programı okur.

## Yaygın Örnekler
Aşağıda `awk` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Bir dosyadaki tüm satırları yazdırma:**
   ```bash
   awk '{print}' dosya.txt
   ```

2. **Belirli bir alanı yazdırma (örneğin, ikinci alan):**
   ```bash
   awk '{print $2}' dosya.txt
   ```

3. **Virgülle ayrılmış bir dosyadan belirli bir alanı yazdırma:**
   ```bash
   awk -F, '{print $1}' dosya.csv
   ```

4. **Bir koşula göre satırları filtreleme (örneğin, 50'den büyük sayılar):**
   ```bash
   awk '$1 > 50' dosya.txt
   ```

5. **Bir dosyadaki satır sayısını bulma:**
   ```bash
   awk 'END {print NR}' dosya.txt
   ```

## İpuçları
- `awk` komutunu kullanırken, alanları doğru bir şekilde ayırmak için uygun ayırıcıyı belirlemeyi unutmayın.
- Karmaşık işlemler için `awk` içinde döngüler ve koşul ifadeleri kullanarak daha gelişmiş programlar yazabilirsiniz.
- `awk`'ın çıktısını başka komutlarla birleştirerek daha etkili veri işleme yapabilirsiniz. Örneğin, `awk` çıktısını `sort` veya `uniq` ile birleştirmek faydalı olabilir.