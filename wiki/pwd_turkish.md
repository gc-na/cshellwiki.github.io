# [Linux] C Shell (csh) pwd Kullanımı: Mevcut dizini gösterir

## Genel Bakış
`pwd` (print working directory) komutu, kullanıcının o anki çalışma dizinini gösterir. Terminalde hangi dizinde bulunduğunuzu hızlıca öğrenmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
pwd [options] [arguments]
```

## Yaygın Seçenekler
- `-L`: Sembolik bağlantılar üzerinden mevcut dizini gösterir.
- `-P`: Fiziksel dizin yolunu gösterir, yani sembolik bağlantıları dikkate almaz.

## Yaygın Örnekler
Aşağıda `pwd` komutunun bazı pratik örnekleri verilmiştir:

1. Mevcut dizini görüntüleme:
   ```csh
   pwd
   ```

2. Fiziksel dizin yolunu görüntüleme:
   ```csh
   pwd -P
   ```

3. Sembolik bağlantılar üzerinden mevcut dizini görüntüleme:
   ```csh
   pwd -L
   ```

## İpuçları
- `pwd` komutunu sık sık kullanarak, terminalde hangi dizinde olduğunuzu kontrol edebilirsiniz.
- Özellikle karmaşık dizin yapılarında çalışırken, `pwd -P` seçeneği ile gerçek dizin yolunu görmek faydalı olabilir.
- Komutun çıktısını başka komutlarla birleştirerek, dizin yolunu kullanabilirsiniz; örneğin, `cd $(pwd)` ile mevcut dizine geri dönebilirsiniz.