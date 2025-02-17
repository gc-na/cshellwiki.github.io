# [Linux] Bash journalctl Kullanımı: Sistem günlüklerini görüntüleme

## Overview
`journalctl`, sistem günlüklerini görüntülemek için kullanılan bir komut satırı aracıdır. Bu komut, systemd tarafından yönetilen günlükleri okumanıza ve analiz etmenize olanak tanır. Günlükler, sistemdeki hizmetlerin, çekirdek olaylarının ve diğer önemli bilgilerin kaydedildiği yerlerdir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
journalctl [options] [arguments]
```

## Common Options
- `-b`: Son sistem başlangıcından itibaren günlükleri gösterir.
- `-f`: Gerçek zamanlı olarak günlükleri takip eder.
- `--since "time"`: Belirtilen zamandan itibaren günlükleri gösterir.
- `--until "time"`: Belirtilen zamana kadar günlükleri gösterir.
- `-u <service>`: Belirtilen hizmete ait günlükleri gösterir.
- `-p <priority>`: Belirtilen öncelik seviyesine sahip günlükleri gösterir (örneğin, `err`, `warning`).

## Common Examples
Aşağıda `journalctl` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Son sistem başlangıcından itibaren günlükleri görüntüleme:
   ```bash
   journalctl -b
   ```

2. Gerçek zamanlı günlük takibi:
   ```bash
   journalctl -f
   ```

3. Belirli bir zamandan itibaren günlükleri görüntüleme:
   ```bash
   journalctl --since "2023-10-01 10:00:00"
   ```

4. Belirli bir hizmetin günlüklerini görüntüleme:
   ```bash
   journalctl -u sshd
   ```

5. Hata seviyesindeki günlükleri görüntüleme:
   ```bash
   journalctl -p err
   ```

## Tips
- Günlükleri daha iyi analiz etmek için `less` gibi bir sayfalayıcı ile birlikte kullanabilirsiniz:
  ```bash
  journalctl | less
  ```
- Belirli bir zaman diliminde günlükleri incelemek için `--since` ve `--until` seçeneklerini bir arada kullanabilirsiniz.
- Günlükleri belirli bir dosyaya yönlendirmek için `>` operatörünü kullanarak çıktıyı kaydedebilirsiniz:
  ```bash
  journalctl > günlükler.txt
  ``` 

Bu bilgilerle `journalctl` komutunu etkili bir şekilde kullanarak sistem günlüklerinizi yönetebilirsiniz.