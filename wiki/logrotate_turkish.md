# [Linux] Bash logrotate Kullanımı: Log dosyalarını döndürme aracı

## Overview
logrotate, sistem yöneticilerinin log dosyalarını yönetmesine yardımcı olan bir komuttur. Bu komut, log dosyalarının boyutunu kontrol altında tutmak, belirli bir süre sonra eski logları silmek veya arşivlemek için kullanılır. Böylece disk alanı tasarrufu sağlanır ve log dosyalarının düzenli bir şekilde saklanması sağlanır.

## Usage
logrotate komutunun temel sözdizimi aşağıdaki gibidir:

```bash
logrotate [options] [arguments]
```

## Common Options
- `-f`: Zorla döndürme. Log dosyalarını döndürmeyi zorlar, yapılandırma dosyasındaki ayarlara bakmaksızın çalışır.
- `-s`: Durum dosyasının yolunu belirtir. logrotate'ın hangi log dosyalarının döndürüldüğünü takip etmesini sağlar.
- `-v`: Ayrıntılı mod. İşlem sırasında daha fazla bilgi gösterir.
- `-d`: Simülasyon modu. Gerçek bir döndürme işlemi yapmadan neler olacağını gösterir.

## Common Examples
Aşağıda logrotate komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Varsayılan yapılandırmayı kullanarak log dosyalarını döndürme
```bash
logrotate /etc/logrotate.conf
```

### Örnek 2: Belirli bir yapılandırma dosyası ile döndürme
```bash
logrotate -f /path/to/custom-logrotate.conf
```

### Örnek 3: Durum dosyasını belirterek döndürme
```bash
logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
```

### Örnek 4: Ayrıntılı modda döndürme
```bash
logrotate -v /etc/logrotate.conf
```

## Tips
- logrotate yapılandırma dosyalarını düzenli olarak kontrol edin ve güncelleyin.
- Log dosyalarınızın boyutunu ve döndürme sıklığını belirlerken sistem gereksinimlerinizi göz önünde bulundurun.
- logrotate'ı otomatik olarak çalıştırmak için cron görevleri ayarlamayı düşünün.