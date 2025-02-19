# [Linux] C Shell (csh) uniq Kullanımı: Tekil satırları listeleme

## Overview
`uniq` komutu, bir dosyada veya standart girişteki ardışık tekrar eden satırları kaldırarak yalnızca benzersiz satırları gösterir. Genellikle sıralı verilerle birlikte kullanılır, çünkü `uniq` yalnızca ardışık tekrarları tespit edebilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```
uniq [options] [arguments]
```

## Common Options
- `-c`: Her benzersiz satırın önüne tekrar sayısını ekler.
- `-d`: Sadece tekrar eden satırları gösterir.
- `-u`: Sadece benzersiz (tekrar etmeyen) satırları gösterir.
- `-i`: Büyük/küçük harf duyarsız olarak karşılaştırma yapar.

## Common Examples
Aşağıda `uniq` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Benzersiz satırları gösterme**:
   ```bash
   sort dosya.txt | uniq
   ```

2. **Tekrar sayısını gösterme**:
   ```bash
   sort dosya.txt | uniq -c
   ```

3. **Sadece tekrar eden satırları gösterme**:
   ```bash
   sort dosya.txt | uniq -d
   ```

4. **Benzersiz satırları büyük/küçük harf duyarsız olarak gösterme**:
   ```bash
   sort dosya.txt | uniq -i
   ```

## Tips
- `uniq` komutunu kullanmadan önce verilerinizi sıralamak için `sort` komutunu kullanmayı unutmayın; aksi takdirde, `uniq` yalnızca ardışık tekrarları kaldırır.
- Büyük/küçük harf duyarsız karşılaştırma yapmak istiyorsanız, `-i` seçeneğini kullanarak sonuçlarınızı daha esnek hale getirebilirsiniz.
- Tekrar eden satırların sayısını görmek istiyorsanız, `-c` seçeneği oldukça kullanışlıdır ve verilerinizi analiz etmenize yardımcı olabilir.