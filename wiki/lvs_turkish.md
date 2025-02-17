# [Linux] Bash lvs Kullanımı: LVM mantıksal hacimlerini listeleme

## Genel Bakış
`lvs` komutu, Linux'ta LVM (Logical Volume Manager) kullanarak oluşturulmuş mantıksal hacimlerin listesini görüntülemek için kullanılır. Bu komut, sistem yöneticilerine ve kullanıcılarına mevcut mantıksal hacimlerin durumunu ve özelliklerini hızlı bir şekilde kontrol etme imkanı sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
lvs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`: Görüntülenecek sütunları belirtir.
- `--units`: Çıktı birimlerini ayarlamak için kullanılır.
- `-a`: Tüm mantıksal hacimleri, gizli olanlar dahil, listeler.
- `-n`: Belirli bir mantıksal hacmin adını belirtmek için kullanılır.

## Yaygın Örnekler
Aşağıda `lvs` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm mantıksal hacimleri listeleme:
   ```bash
   lvs
   ```

2. Belirli bir mantıksal hacmi listeleme:
   ```bash
   lvs -n hacim_adı
   ```

3. Çıktıda belirli sütunları görüntüleme:
   ```bash
   lvs -o +size,devices
   ```

4. Tüm mantıksal hacimleri gizli olanlar dahil listeleme:
   ```bash
   lvs -a
   ```

5. Çıktı birimlerini ayarlama:
   ```bash
   lvs --units g
   ```

## İpuçları
- `lvs` komutunu sık sık kullanıyorsanız, çıktıyı daha okunabilir hale getirmek için `--units` seçeneğini kullanarak birimleri ayarlayabilirsiniz.
- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  lvs > lvs_output.txt
  ```
- `man lvs` komutunu kullanarak daha fazla bilgi ve seçenekler hakkında detaylı bilgi alabilirsiniz.