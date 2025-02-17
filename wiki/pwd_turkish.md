# [Linux] Bash pwd Kullanımı: Mevcut dizini gösterir

## Genel Bakış
`pwd` (print working directory) komutu, kullanıcıların terminalde bulundukları mevcut dizinin tam yolunu gösterir. Bu komut, dosya sisteminde hangi dizinde çalıştığınızı anlamanıza yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
pwd [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-L`: Mantıksal dizini gösterir. (Varsayılan)
- `-P`: Fiziksel dizini gösterir. (Sembolik bağlantıları takip etmez)

## Yaygın Örnekler
1. Mevcut dizini görüntülemek için:
   ```bash
   pwd
   ```

2. Fiziksel dizini görüntülemek için:
   ```bash
   pwd -P
   ```

3. Mantıksal dizini görüntülemek için:
   ```bash
   pwd -L
   ```

## İpuçları
- `pwd` komutunu sık sık kullanarak, hangi dizinde çalıştığınızı kolayca kontrol edebilirsiniz.
- Özellikle karmaşık dizin yapılarında çalışıyorsanız, `pwd -P` seçeneği ile sembolik bağlantılardan kaçınarak gerçek dizin yolunu öğrenmek faydalı olabilir.
- `pwd` komutunu bir betikte kullanarak, betiğin hangi dizinde çalıştığını kaydedebilirsiniz.