# [Unix] C Shell (csh) history Kullanımı: Komut geçmişini görüntüleme

## Genel Bakış
`history` komutu, C Shell (csh) ortamında daha önce çalıştırılmış komutların listesini görüntülemeye yarar. Bu komut, kullanıcıların geçmişteki komutlarını hatırlamalarına ve tekrar kullanmalarına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
history [options] [arguments]
```

## Yaygın Seçenekler
- `-c`: Geçmişi temizler.
- `-n`: Geçmiş dosyasını okur ve mevcut geçmişe ekler.
- `-r`: Geçmiş dosyasını okur ve geçmişi günceller.
- `-w`: Geçmişi dosyaya yazar.

## Yaygın Örnekler
1. Tüm geçmişi görüntülemek için:
   ```csh
   history
   ```

2. Geçmişteki son 10 komutu görüntülemek için:
   ```csh
   history 10
   ```

3. Geçmişi temizlemek için:
   ```csh
   history -c
   ```

4. Geçmiş dosyasını güncellemek için:
   ```csh
   history -w
   ```

## İpuçları
- Geçmişteki komutları hızlıca tekrar çalıştırmak için `!` operatörünü kullanabilirsiniz. Örneğin, `!5` komutu, geçmişteki 5. komutu tekrar çalıştırır.
- Geçmişi düzenli olarak temizlemek, gereksiz karmaşayı önler ve daha verimli bir çalışma ortamı sağlar.
- Geçmiş dosyasını yedeklemek, önemli komutları kaybetmemek için iyi bir uygulamadır.