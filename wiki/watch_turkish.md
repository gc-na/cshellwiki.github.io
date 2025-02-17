# [Linux] Bash watch Kullanımı: Komutların sürekli izlenmesi

## Overview
`watch` komutu, belirli bir komutu belirli aralıklarla çalıştırarak çıktısını sürekli olarak görüntülemenizi sağlar. Bu, sistem durumunu izlemek veya belirli bir komutun çıktısındaki değişiklikleri takip etmek için oldukça yararlıdır.

## Usage
Temel kullanım şekli aşağıdaki gibidir:

```
watch [options] [arguments]
```

## Common Options
- `-n, --interval`: Komutun ne sıklıkta çalıştırılacağını belirler (saniye cinsinden).
- `-d, --differences`: Çıktıdaki değişiklikleri vurgular.
- `-t, --no-title`: Başlık satırını gizler.
- `-h, --help`: Yardım bilgilerini gösterir.

## Common Examples
1. Belirli bir dosyanın içeriğini her 2 saniyede bir kontrol etme:
   ```bash
   watch -n 2 cat /var/log/syslog
   ```

2. Bir dizindeki dosya sayısını her 5 saniyede bir görüntüleme:
   ```bash
   watch -n 5 ls -1 | wc -l
   ```

3. Sistem kaynak kullanımını izleme:
   ```bash
   watch -d free -h
   ```

4. Belirli bir servisin durumunu kontrol etme:
   ```bash
   watch -n 10 systemctl status apache2
   ```

## Tips
- `-d` seçeneğini kullanarak çıktınızdaki değişiklikleri kolayca fark edebilirsiniz.
- İzlemek istediğiniz komutun çıktısının çok büyük olmamasına dikkat edin; aksi takdirde ekran karmaşıklaşabilir.
- `-t` seçeneği ile başlık satırını gizleyerek daha fazla alan kazanabilirsiniz.