# [Linux] Bash parted Kullanımı: Disk bölümlerini yönetme aracı

## Genel Bakış
`parted`, disk bölümlerini yönetmek için kullanılan bir komut satırı aracıdır. Bu araç, disk bölümlerini oluşturma, silme, boyutlandırma ve düzenleme gibi işlemleri gerçekleştirmeye olanak tanır. `parted`, özellikle büyük disklerde ve farklı dosya sistemlerinde çalışırken oldukça kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
parted [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`, `--list`: Tüm diskleri ve bölümleri listele.
- `mkpart`: Yeni bir bölüm oluştur.
- `rm`: Belirtilen bölümü sil.
- `resizepart`: Mevcut bir bölümün boyutunu değiştir.
- `print`: Mevcut bölümleri ve bilgilerini göster.

## Yaygın Örnekler
1. **Tüm diskleri listeleme:**
   ```bash
   parted -l
   ```

2. **Yeni bir bölüm oluşturma:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Bir bölümü silme:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Bir bölümü boyutlandırma:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Mevcut bölümleri görüntüleme:**
   ```bash
   parted /dev/sda print
   ```

## İpuçları
- `parted` komutunu kullanmadan önce, önemli verilerinizi yedeklemeyi unutmayın.
- Disk bölümleri üzerinde işlem yaparken dikkatli olun; yanlış bir işlem veri kaybına yol açabilir.
- `parted` komutunu çalıştırmadan önce, hangi disk üzerinde işlem yapacağınızı net bir şekilde belirleyin.