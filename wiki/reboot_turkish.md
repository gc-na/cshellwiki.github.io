# [Linux] Bash reboot Kullanımı: Sistemi yeniden başlatma

## Genel Bakış
`reboot` komutu, Linux tabanlı işletim sistemlerinde sistemi yeniden başlatmak için kullanılır. Bu komut, sistemin düzgün bir şekilde kapanmasını ve ardından yeniden açılmasını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
reboot [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Sistemi zorla yeniden başlatır, açık olan işlemleri kapatmadan.
- `-p`: Sistemi kapatır ve güç kaynağını kapatır.
- `-n`: Sistemi yeniden başlatmadan önce dosya sistemlerini kontrol etmez.

## Yaygın Örnekler
1. Basit bir yeniden başlatma:
   ```bash
   reboot
   ```

2. Sistemi zorla yeniden başlatma:
   ```bash
   reboot -f
   ```

3. Sistemi kapatıp güç kaynağını kapatma:
   ```bash
   reboot -p
   ```

4. Yeniden başlatma işlemi için bir zamanlayıcı ayarlama (örneğin, 1 dakika sonra):
   ```bash
   shutdown -r +1
   ```

## İpuçları
- Yeniden başlatma işlemi yapmadan önce açık olan dosyalarınızı kaydetmeyi unutmayın.
- Sunucu ortamlarında `-f` seçeneğini kullanmadan önce dikkatli olun, çünkü bu açık işlemleri kapatabilir.
- Sistem güncellemeleri sonrası genellikle yeniden başlatma gereklidir, bu nedenle güncellemeleri tamamladıktan sonra `reboot` komutunu kullanmayı unutmayın.