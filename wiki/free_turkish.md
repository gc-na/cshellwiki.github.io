# [Linux] Bash free komutu: Bellek kullanımını görüntüleme

## Genel Bakış
`free` komutu, sistemdeki bellek kullanımını görüntülemek için kullanılır. Bu komut, toplam bellek, kullanılabilir bellek, boş bellek ve takas alanı gibi bilgileri sağlar. Sistem yöneticileri ve kullanıcılar, bellek durumunu hızlı bir şekilde kontrol etmek için bu komutu sıklıkla kullanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
free [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Bellek miktarlarını insan tarafından okunabilir formatta gösterir (örneğin, KB, MB, GB).
- `-m`: Bellek miktarlarını megabayt cinsinden gösterir.
- `-g`: Bellek miktarlarını gigabayt cinsinden gösterir.
- `-s [saniye]`: Belirtilen saniye aralıklarıyla sürekli güncellemeler yapar.
- `-t`: Toplam bellek kullanımını gösterir.

## Yaygın Örnekler
1. Temel bellek durumu görüntüleme:
   ```bash
   free
   ```

2. İnsan tarafından okunabilir formatta bellek durumu görüntüleme:
   ```bash
   free -h
   ```

3. Bellek kullanımını megabayt cinsinden görüntüleme:
   ```bash
   free -m
   ```

4. Her 5 saniyede bir bellek durumunu güncelleme:
   ```bash
   free -s 5
   ```

5. Toplam bellek kullanımını gösterme:
   ```bash
   free -t
   ```

## İpuçları
- `free -h` komutunu kullanarak bellek kullanımını daha kolay anlamak için insan tarafından okunabilir formatta görüntüleyin.
- Bellek kullanımını izlemek için `free -s` seçeneğini kullanarak belirli aralıklarla güncellemeleri takip edebilirsiniz.
- Sisteminizde bellek sorunları yaşıyorsanız, `free` komutunu düzenli olarak kontrol etmek, sorunları tespit etmenize yardımcı olabilir.