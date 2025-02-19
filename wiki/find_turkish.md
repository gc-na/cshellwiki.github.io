# [Linux] C Shell (csh) find Kullanımı: Dosya adlarını bulma

## Genel Bakış
`find` komutu, belirli bir dizin altında dosya ve dizinleri aramak için kullanılır. Kullanıcıların belirli kriterlere göre dosyaları bulmasını sağlar, bu da dosya yönetimini kolaylaştırır.

## Kullanım
Temel sözdizimi şu şekildedir:

```csh
find [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-name`: Belirtilen ada sahip dosyaları bulur.
- `-type`: Belirli bir dosya türünü arar (örneğin, `f` dosya, `d` dizin).
- `-size`: Belirli bir boyutta dosyaları bulur.
- `-mtime`: Belirli bir süre önce değiştirilmiş dosyaları bulur.
- `-exec`: Bulunan dosyalar üzerinde bir komut çalıştırır.

## Yaygın Örnekler
Aşağıda `find` komutunun bazı pratik örnekleri verilmiştir:

1. Belirli bir dizinde belirli bir ada sahip dosyaları bulma:
   ```csh
   find /path/to/directory -name "dosya.txt"
   ```

2. Sadece dizinleri bulma:
   ```csh
   find /path/to/directory -type d
   ```

3. 1 MB'den büyük dosyaları bulma:
   ```csh
   find /path/to/directory -size +1M
   ```

4. Son 7 gün içinde değiştirilmiş dosyaları bulma:
   ```csh
   find /path/to/directory -mtime -7
   ```

5. Bulunan dosyalar üzerinde bir komut çalıştırma (örneğin, silme):
   ```csh
   find /path/to/directory -name "*.tmp" -exec rm {} \;
   ```

## İpuçları
- `find` komutunu kullanırken, arama yaptığınız dizini doğru belirlemek önemlidir.
- Arama sonuçlarını daha iyi yönetmek için `-print` seçeneğini kullanarak sonuçları görüntüleyebilirsiniz.
- `find` komutunu diğer komutlarla birleştirerek daha karmaşık işlemler gerçekleştirebilirsiniz. Örneğin, `grep` ile birlikte kullanarak belirli içeriklere sahip dosyaları bulabilirsiniz.