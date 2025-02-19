# [Linux] C Shell (csh) head Kullanımı: Dosya içeriğinin başlangıcını görüntüleme

## Genel Bakış
`head` komutu, bir dosyanın en üst kısmındaki belirli sayıda satırı görüntülemek için kullanılır. Genellikle, dosyanın içeriğini hızlıca incelemek veya büyük dosyaların sadece ilk kısımlarını görmek için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
head [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n [sayı]`: Görüntülenecek satır sayısını belirtir. Varsayılan olarak ilk 10 satırı gösterir.
- `-q`: Çıktı başlıklarını gizler. Birden fazla dosya belirtilirse, her dosya için başlık gösterilmez.
- `-c [bayt]`: Belirtilen bayt sayısını görüntüler.

## Yaygın Örnekler
Aşağıda `head` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Bir dosyanın ilk 10 satırını görüntüleme (varsayılan):
   ```csh
   head dosya.txt
   ```

2. Bir dosyanın ilk 5 satırını görüntüleme:
   ```csh
   head -n 5 dosya.txt
   ```

3. Birden fazla dosyanın ilk 10 satırını görüntüleme:
   ```csh
   head dosya1.txt dosya2.txt
   ```

4. Bir dosyanın ilk 20 baytını görüntüleme:
   ```csh
   head -c 20 dosya.txt
   ```

## İpuçları
- `head` komutunu, büyük dosyaların içeriğini hızlıca gözden geçirmek için kullanabilirsiniz.
- Birden fazla dosya ile çalışırken, hangi dosyanın içeriğini görüntülediğinizi anlamak için `-q` seçeneğini kullanarak başlıkları gizleyebilirsiniz.
- `head` komutunu, `tail` komutuyla birlikte kullanarak dosyanın hem başlangıcını hem de sonunu inceleyebilirsiniz.