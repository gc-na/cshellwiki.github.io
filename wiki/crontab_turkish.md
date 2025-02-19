# [Linux] C Shell (csh) crontab Kullanımı: Zamanlanmış görevleri yönetme

## Genel Bakış
`crontab` komutu, belirli zaman dilimlerinde otomatik olarak çalıştırılacak görevleri tanımlamak için kullanılır. Bu komut, sistem yöneticileri ve kullanıcılar tarafından, tekrarlayan görevleri kolayca planlamak amacıyla yaygın olarak kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
crontab [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Mevcut crontab dosyasını düzenlemek için kullanılır.
- `-l`: Mevcut crontab dosyasını listelemek için kullanılır.
- `-r`: Mevcut crontab dosyasını silmek için kullanılır.
- `-i`: `-r` seçeneği ile birlikte kullanıldığında, silme işlemi öncesinde onay ister.

## Yaygın Örnekler
Aşağıda `crontab` komutunun bazı pratik örnekleri verilmiştir:

1. **Crontab dosyasını düzenleme:**
   ```bash
   crontab -e
   ```

2. **Mevcut crontab dosyasını görüntüleme:**
   ```bash
   crontab -l
   ```

3. **Crontab dosyasını silme:**
   ```bash
   crontab -r
   ```

4. **Her gün saat 2'de bir yedekleme script'ini çalıştırma:**
   ```bash
   0 2 * * * /path/to/backup_script.sh
   ```

5. **Her 5 dakikada bir bir log dosyasını temizleme:**
   ```bash
   */5 * * * * /path/to/clear_log.sh
   ```

## İpuçları
- Görevlerinizi düzenli olarak kontrol edin ve gereksiz olanları temizleyin.
- Görevlerinizi test etmek için başlangıçta daha kısa zaman dilimleri kullanın.
- Log dosyalarını kullanarak görevlerinizin çıktısını kaydedin; bu, sorunları teşhis etmenize yardımcı olur.