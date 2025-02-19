# [Linux] C Shell (csh) free kullanımı: Bellek durumu görüntüleme

## Genel Bakış
`free` komutu, sistemdeki bellek kullanımını gösterir. Bu komut, toplam bellek, kullanılabilir bellek, boş bellek ve takas alanı gibi bilgileri sağlar. Sistem yöneticileri ve kullanıcılar, bellek durumunu izlemek için bu komutu sıklıkla kullanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
free [options] [arguments]
```

## Yaygın Seçenekler
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB).
- `-m`: Bellek bilgilerini megabayt cinsinden gösterir.
- `-g`: Bellek bilgilerini gigabayt cinsinden gösterir.
- `-s [saniye]`: Belirtilen saniye aralıklarıyla sürekli güncellenen bir çıktı sağlar.

## Yaygın Örnekler
Aşağıda `free` komutunun bazı pratik örnekleri bulunmaktadır:

1. Temel bellek bilgilerini görüntüleme:
   ```csh
   free
   ```

2. İnsan tarafından okunabilir formatta bellek bilgilerini görüntüleme:
   ```csh
   free -h
   ```

3. Bellek bilgilerini megabayt cinsinden görüntüleme:
   ```csh
   free -m
   ```

4. Bellek bilgilerini gigabayt cinsinden görüntüleme:
   ```csh
   free -g
   ```

5. Her 5 saniyede bir güncellenen bellek bilgilerini görüntüleme:
   ```csh
   free -s 5
   ```

## İpuçları
- `free -h` komutunu kullanarak bellek kullanımını daha kolay anlayabilirsiniz.
- Bellek kullanımını izlemek için `free -s` seçeneği ile bir terminal penceresi açarak sürekli güncellemeleri takip edebilirsiniz.
- Bellek kullanımını analiz ederken, takas alanının durumunu da göz önünde bulundurmak önemlidir; bu nedenle `free` çıktısındaki "Swap" bölümünü inceleyin.