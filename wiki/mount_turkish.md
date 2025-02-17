# [Linux] Bash mount Kullanımı: Dosya sistemlerini bağlama

## Genel Bakış
`mount` komutu, bir dosya sistemini belirli bir dizine bağlamak için kullanılır. Bu işlem, dosya sisteminin içeriğine erişim sağlamanızı ve dosyaları yönetmenizi mümkün kılar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mount [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-t <tip>`: Bağlanacak dosya sisteminin türünü belirtir (örneğin, ext4, ntfs).
- `-o <seçenekler>`: Bağlama işlemi için özel seçenekler tanımlar (örneğin, `ro` sadece okuma için, `rw` okuma/yazma için).
- `-a`: `/etc/fstab` dosyasındaki tüm dosya sistemlerini bağlar.
- `-r`: Dosya sistemini yalnızca okuma modunda bağlar.

## Yaygın Örnekler
1. **Bir dosya sistemini bağlamak:**
   ```bash
   mount /dev/sdb1 /mnt/mydrive
   ```

2. **NTFS dosya sistemini bağlamak:**
   ```bash
   mount -t ntfs-3g /dev/sdc1 /mnt/ntfsdrive
   ```

3. **Sadece okuma modunda bağlamak:**
   ```bash
   mount -o ro /dev/sda1 /mnt/readonly
   ```

4. **Tüm dosya sistemlerini bağlamak:**
   ```bash
   mount -a
   ```

## İpuçları
- Bağlama işlemi yapmadan önce, bağlanacak dizinin var olduğundan emin olun.
- Dosya sistemini çıkarmadan önce, tüm dosyaların kapatıldığından ve dosya sisteminin kullanılmadığından emin olun.
- `df -h` komutunu kullanarak bağlı dosya sistemlerinin durumunu kontrol edebilirsiniz.