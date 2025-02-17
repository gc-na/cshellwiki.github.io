# [Linux] Bash last komutu: Kullanıcı oturum geçmişini görüntüleme

## Genel Bakış
`last` komutu, sistemdeki kullanıcı oturumlarının geçmişini görüntülemek için kullanılır. Bu komut, kullanıcıların ne zaman giriş yaptığını ve ne zaman çıktığını gösterir. Ayrıca, sistemin yeniden başlatıldığı zamanları da listeleyebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
last [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Kullanıcıların giriş yaptığı son IP adresini gösterir.
- `-n [sayı]`: Belirtilen sayıda en son oturumu gösterir.
- `-x`: Sistem kapanışlarını ve yeniden başlatmalarını da gösterir.
- `-R`: Sunucu adını göstermeden sadece kullanıcı adlarını ve zaman bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `last` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm kullanıcı oturumlarını görüntüleme:
   ```bash
   last
   ```

2. Son 5 oturumu görüntüleme:
   ```bash
   last -n 5
   ```

3. Kullanıcı adıyla belirli bir kullanıcının oturum geçmişini görüntüleme:
   ```bash
   last kullanıcı_adı
   ```

4. Kullanıcıların giriş yaptığı son IP adreslerini gösterme:
   ```bash
   last -a
   ```

5. Sistem kapanış ve yeniden başlatma geçmişini görüntüleme:
   ```bash
   last -x
   ```

## İpuçları
- `last` komutunu kullanarak sistemdeki kullanıcı etkinliğini izleyebilir ve güvenlik denetimleri yapabilirsiniz.
- Uzun bir oturum geçmişini incelemek istiyorsanız, çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  last > oturum_gecmisi.txt
  ```
- Çıktıyı daha okunabilir hale getirmek için `less` veya `more` komutları ile birleştirebilirsiniz:
  ```bash
  last | less
  ```