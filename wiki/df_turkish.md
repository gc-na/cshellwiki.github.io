# [Linux] Bash df Kullanımı: Disk alanı bilgisi görüntüleme

## Genel Bakış
`df` komutu, sistemdeki dosya sistemlerinin disk alanı kullanımını gösterir. Bu komut, her bir dosya sisteminin toplam, kullanılan ve boş alan miktarını görüntüleyerek kullanıcıların disk alanı yönetimini kolaylaştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
df [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: İnsan tarafından okunabilir formatta (örneğin, KB, MB, GB) çıktı verir.
- `-T`: Dosya sisteminin türünü gösterir.
- `-a`: Tüm dosya sistemlerini, boş olanlar dahil, gösterir.
- `-i`: İnode kullanımını gösterir.

## Yaygın Örnekler
Aşağıda `df` komutunun bazı pratik örnekleri verilmiştir:

1. **Temel Disk Kullanımını Görüntüleme:**
   ```bash
   df
   ```

2. **İnsan Okunabilir Format:**
   ```bash
   df -h
   ```

3. **Dosya Sistemi Türünü Gösterme:**
   ```bash
   df -T
   ```

4. **Tüm Dosya Sistemlerini Gösterme:**
   ```bash
   df -a
   ```

5. **İnode Kullanımını Görüntüleme:**
   ```bash
   df -i
   ```

## İpuçları
- `df -h` kullanarak çıktıyı daha okunabilir hale getirin, böylece alanları KB, MB veya GB olarak görebilirsiniz.
- Disk alanı sorunlarını çözmek için `df` çıktısını düzenli olarak kontrol edin.
- Belirli bir dosya sisteminin kullanımını görmek için, dosya sisteminin yolunu argüman olarak verebilirsiniz. Örneğin:
  ```bash
  df -h /home
  ```