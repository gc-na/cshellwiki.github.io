# [Linux] C Shell (csh) journalctl Kullanımı: Sistem günlüklerini görüntüleme

## Genel Bakış
`journalctl`, sistem günlüklerini görüntülemek için kullanılan bir komuttur. Bu komut, sistemdeki hizmetlerin, çekirdek mesajlarının ve diğer günlüklerin kaydedildiği `systemd` günlük sistemine erişim sağlar. Kullanıcılar, günlükleri filtreleyebilir, sıralayabilir ve belirli bir zaman dilimindeki olayları inceleyebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
journalctl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-b`: Son sistem başlangıcından itibaren günlükleri gösterir.
- `-f`: Gerçek zamanlı olarak günlükleri takip eder.
- `--since "tarih"`: Belirtilen tarihten itibaren günlükleri gösterir.
- `--until "tarih"`: Belirtilen tarihe kadar günlükleri gösterir.
- `-p [seviyeler]`: Belirtilen öncelik seviyesine göre günlükleri filtreler (örneğin, `-p err` sadece hata mesajlarını gösterir).

## Yaygın Örnekler
Aşağıda `journalctl` komutunun bazı pratik örnekleri bulunmaktadır:

1. Son sistem başlangıcından itibaren günlükleri görüntüleme:
   ```bash
   journalctl -b
   ```

2. Gerçek zamanlı günlük takibi:
   ```bash
   journalctl -f
   ```

3. Belirli bir tarihten itibaren günlükleri görüntüleme:
   ```bash
   journalctl --since "2023-10-01"
   ```

4. Belirli bir tarihe kadar günlükleri görüntüleme:
   ```bash
   journalctl --until "2023-10-10"
   ```

5. Sadece hata mesajlarını görüntüleme:
   ```bash
   journalctl -p err
   ```

## İpuçları
- Günlükleri daha iyi analiz etmek için `less` komutuyla birleştirerek sayfalandırabilirsiniz:
  ```bash
  journalctl | less
  ```
- Belirli bir hizmete ait günlükleri görüntülemek için hizmet adını belirtebilirsiniz:
  ```bash
  journalctl -u [hizmet_adı]
  ```
- Günlükleri belirli bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  journalctl > günlükler.txt
  ```

Bu bilgilerle `journalctl` komutunu etkili bir şekilde kullanabilir ve sistem günlüklerinizi yönetebilirsiniz.