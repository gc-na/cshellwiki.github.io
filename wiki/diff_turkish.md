# [Linux] Bash diff Kullanımı: İki dosya arasındaki farkları karşılaştırma

## Genel Bakış
`diff` komutu, iki dosya arasındaki farklılıkları karşılaştırmak için kullanılır. Bu komut, metin dosyalarını karşılaştırarak, hangi satırların eklendiğini, silindiğini veya değiştirildiğini gösterir. Yazılım geliştirme süreçlerinde, özellikle sürüm kontrol sistemlerinde sıkça kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
diff [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: Birleştirilmiş formatta çıktı verir, bu format daha okunabilir bir görünüm sunar.
- `-i`: Büyük/küçük harf duyarlılığını göz ardı eder.
- `-w`: Boşlukları göz ardı eder, sadece anlamlı farklılıkları gösterir.
- `-r`: Dizindeki alt dizinlerdeki dosyaları da karşılaştırır.

## Yaygın Örnekler

### İki dosya arasındaki farkları gösterme
```bash
diff dosya1.txt dosya2.txt
```

### Birleştirilmiş formatta farkları gösterme
```bash
diff -u dosya1.txt dosya2.txt
```

### Büyük/küçük harf duyarlılığını göz ardı etme
```bash
diff -i dosya1.txt dosya2.txt
```

### Boşlukları göz ardı ederek karşılaştırma
```bash
diff -w dosya1.txt dosya2.txt
```

### Alt dizinlerdeki dosyaları karşılaştırma
```bash
diff -r dizin1/ dizin2/
```

## İpuçları
- `diff` çıktısını daha iyi anlamak için `-u` seçeneğini kullanarak birleştirilmiş formatta görüntüleyin.
- Farklılıkları daha iyi analiz etmek için `diff` çıktısını bir dosyaya yönlendirebilirsiniz:
  ```bash
  diff dosya1.txt dosya2.txt > farklar.txt
  ```
- `diff` komutunu sık kullanılan dosya karşılaştırmalarında bir alias olarak tanımlamak, kullanımınızı kolaylaştırabilir. Örneğin:
  ```bash
  alias d='diff -u'
  ```

Bu bilgilerle, `diff` komutunu etkili bir şekilde kullanarak dosyalar arasındaki farklılıkları kolayca tespit edebilirsiniz.