# [Linux] C Shell (csh) comm kullanımı: İki dosya arasındaki farklılıkları karşılaştırma

## Genel Bakış
`comm` komutu, iki sıralı dosya arasındaki satırları karşılaştırarak ortak ve farklı satırları gösterir. Bu komut, özellikle metin dosyaları arasındaki farkları analiz etmek için kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
comm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-1`: İlk dosyada bulunan ancak ikinci dosyada bulunmayan satırları göstermez.
- `-2`: İkinci dosyada bulunan ancak ilk dosyada bulunmayan satırları göstermez.
- `-3`: Her iki dosyada da bulunan satırları göstermez.
- `-i`: Büyük/küçük harf duyarsız karşılaştırma yapar.

## Yaygın Örnekler
1. İki dosya arasındaki tüm farklılıkları görmek için:
   ```csh
   comm dosya1.txt dosya2.txt
   ```

2. Sadece `dosya1.txt`'te bulunan satırları listelemek için:
   ```csh
   comm -13 dosya1.txt dosya2.txt
   ```

3. Sadece `dosya2.txt`'te bulunan satırları listelemek için:
   ```csh
   comm -23 dosya1.txt dosya2.txt
   ```

4. Her iki dosyada da bulunan satırları hariç tutarak karşılaştırmak için:
   ```csh
   comm -12 dosya1.txt dosya2.txt
   ```

## İpuçları
- Dosyaların sıralı olduğundan emin olun; `comm` komutu, sıralı dosyalarla en iyi şekilde çalışır. Gerekirse `sort` komutunu kullanarak dosyaları sıralayın.
- Büyük/küçük harf duyarsız karşılaştırma yapmak istiyorsanız `-i` seçeneğini kullanmayı unutmayın.
- Sonuçları bir dosyaya kaydetmek için çıktı yönlendirmesini kullanabilirsiniz:
  ```csh
  comm dosya1.txt dosya2.txt > farklar.txt
  ```