# [Linux] C Shell (csh) mv Kullanımı: Dosya ve dizinleri taşımak veya yeniden adlandırmak

## Genel Bakış
`mv` komutu, dosyaları ve dizinleri taşımak veya yeniden adlandırmak için kullanılır. Bu komut, belirtilen kaynak dosyayı hedef konuma taşır veya dosyanın adını değiştirir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
mv [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Hedef dosya mevcutsa, üzerine yazmadan önce kullanıcıdan onay ister.
- `-f`: Hedef dosya mevcutsa, üzerine yazmadan onay istemez.
- `-u`: Sadece kaynak dosya, hedef dosyadan daha yeni ise taşır.

## Yaygın Örnekler
Aşağıda `mv` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Bir dosyayı başka bir dizine taşımak:
   ```csh
   mv dosya.txt /hedef/dizin/
   ```

2. Bir dosyanın adını değiştirmek:
   ```csh
   mv eski_ad.txt yeni_ad.txt
   ```

3. Bir dosyayı başka bir dizine taşırken adını değiştirmek:
   ```csh
   mv dosya.txt /hedef/dizin/yeni_ad.txt
   ```

4. Hedef dosya mevcutsa, üzerine yazmadan önce onay istemek:
   ```csh
   mv -i dosya.txt /hedef/dizin/
   ```

## İpuçları
- `mv` komutunu kullanmadan önce, hedef dizinin doğru olduğundan emin olun.
- Dosya adlarını değiştirmek için `-i` seçeneğini kullanarak yanlışlıkla dosyaların üzerine yazmayı önleyebilirsiniz.
- Sık kullanılan dizinlere taşımak için, tam yol yerine kısa yollar kullanmayı düşünün.