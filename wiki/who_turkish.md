# [Linux] Bash who Kullanımı: Kullanıcı oturumlarını görüntüleme

## Genel Bakış
`who` komutu, sistemde oturum açmış olan kullanıcıların listesini görüntülemek için kullanılır. Bu komut, kullanıcı adı, oturum açma zamanı ve terminal bilgileri gibi detayları sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
who [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bilgileri gösterir, kullanıcıların yanı sıra sistem bilgilerini de içerir.
- `-b`: Sistemin en son ne zaman yeniden başlatıldığını gösterir.
- `-q`: Sadece kullanıcı adlarını ve toplam kullanıcı sayısını gösterir.
- `--help`: Komut hakkında yardım bilgisi gösterir.

## Yaygın Örnekler
Aşağıda `who` komutunun bazı pratik kullanımları bulunmaktadır:

1. Sistemdeki tüm oturum açmış kullanıcıları görüntüleme:
   ```bash
   who
   ```

2. Sistemin en son ne zaman yeniden başlatıldığını öğrenme:
   ```bash
   who -b
   ```

3. Sadece kullanıcı adlarını ve toplam sayısını gösterme:
   ```bash
   who -q
   ```

4. Tüm kullanıcı bilgilerini detaylı bir şekilde görüntüleme:
   ```bash
   who -a
   ```

## İpuçları
- `who` komutunu sık sık kullanarak sistemdeki aktif kullanıcıları takip edebilirsiniz.
- Eğer belirli bir kullanıcı hakkında bilgi almak istiyorsanız, `grep` ile birleştirerek filtreleme yapabilirsiniz:
  ```bash
  who | grep kullanıcı_adı
  ```
- `who` komutunu, sistem yönetimi ve güvenlik denetimleri için düzenli olarak kullanmak iyi bir uygulamadır.