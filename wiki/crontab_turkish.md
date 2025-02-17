# [Linux] Bash crontab Kullanımı: Zamanlanmış görevleri yönetme

## Genel Bakış
`crontab` komutu, belirli zamanlarda otomatik olarak çalıştırılacak görevleri tanımlamak için kullanılır. Bu komut, sistem yöneticileri ve kullanıcılar tarafından, düzenli olarak yapılması gereken işler için zamanlama ayarlamak amacıyla yaygın olarak kullanılır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
crontab [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Kullanıcının crontab dosyasını düzenlemesine olanak tanır.
- `-l`: Kullanıcının mevcut crontab dosyasını listelemesini sağlar.
- `-r`: Kullanıcının crontab dosyasını siler.
- `-i`: `-r` seçeneği ile birlikte kullanıldığında, silme işlemi öncesinde onay ister.

## Yaygın Örnekler
Aşağıda `crontab` komutunun bazı pratik örnekleri bulunmaktadır:

1. Her gün saat 2:30'da bir yedekleme scriptini çalıştırmak:
   ```bash
   30 2 * * * /path/to/backup.sh
   ```

2. Her Pazartesi saat 14:00'te bir güncelleme kontrolü yapmak:
   ```bash
   0 14 * * 1 /path/to/update-check.sh
   ```

3. Her 5 dakikada bir bir log dosyasını temizlemek:
   ```bash
   */5 * * * * /path/to/cleanup-log.sh
   ```

4. Her ayın ilk günü saat 00:01'de rapor oluşturmak:
   ```bash
   1 0 1 * * /path/to/report.sh
   ```

## İpuçları
- Crontab dosyasını düzenlerken dikkatli olun; yanlış bir zamanlama, istenmeyen sonuçlara yol açabilir.
- Görevlerin çıktısını bir log dosyasına yönlendirmek için `>> /path/to/logfile.log 2>&1` ekleyebilirsiniz.
- Zamanlama ifadelerini test etmek için `cron` yerine `sleep` komutunu kullanarak kısa süreli testler yapabilirsiniz.