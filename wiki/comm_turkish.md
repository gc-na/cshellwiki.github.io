# [Linux] Bash comm Kullanımı: İki dosya arasındaki farklılıkları karşılaştırma

## Genel Bakış
`comm` komutu, iki sıralı dosya arasındaki satırları karşılaştırmak için kullanılır. Bu komut, her iki dosyada bulunan, yalnızca birinde bulunan ve her iki dosyada da bulunan satırları ayırarak çıktıyı düzenler.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
comm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-1`: İlk dosyada bulunan satırları gizler.
- `-2`: İkinci dosyada bulunan satırları gizler.
- `-3`: Her iki dosyada da bulunan satırları gizler.
- `-i`: Büyük/küçük harf duyarsız karşılaştırma yapar.
- `-u`: Sadece benzersiz satırları gösterir.

## Yaygın Örnekler
1. **İki dosya arasındaki tüm farklılıkları gösterme:**
   ```bash
   comm dosya1.txt dosya2.txt
   ```

2. **Sadece birinci dosyada bulunan satırları gösterme:**
   ```bash
   comm -13 dosya1.txt dosya2.txt
   ```

3. **Sadece ikinci dosyada bulunan satırları gösterme:**
   ```bash
   comm -12 dosya1.txt dosya2.txt
   ```

4. **Büyük/küçük harf duyarsız karşılaştırma yapma:**
   ```bash
   comm -i dosya1.txt dosya2.txt
   ```

## İpuçları
- `comm` komutunu kullanmadan önce dosyaların sıralı olduğundan emin olun. Sıralı değillerse, `sort` komutunu kullanarak dosyaları sıralayabilirsiniz.
- Çıktıyı daha okunabilir hale getirmek için `-1`, `-2` veya `-3` seçeneklerini kullanarak gereksiz bilgileri gizleyebilirsiniz.
- `comm` komutunu, dosya karşılaştırmaları için bir betik içinde otomatikleştirmek, düzenli dosya kontrolü yaparken faydalı olabilir.