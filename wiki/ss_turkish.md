# [Linux] Bash ss Kullanımı: Ağ bağlantılarını görüntüleme

## Overview
`ss` komutu, Linux sistemlerinde ağ bağlantılarını görüntülemek için kullanılan bir araçtır. Bu komut, aktif bağlantıları, dinleme soketlerini ve diğer ağ istatistiklerini hızlı bir şekilde gösterir. `ss`, `netstat` komutuna göre daha hızlı ve daha ayrıntılı bilgiler sunar.

## Usage
Temel sözdizimi şu şekildedir:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-l`: Dinleme durumundaki soketleri listeler.
- `-p`: Bağlantılarla ilişkili süreçleri gösterir.
- `-n`: Adres ve port numaralarını sayısal olarak gösterir.

## Common Examples
Aşağıda `ss` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Tüm Aktif Bağlantıları Görüntüleme
```bash
ss
```

### TCP Bağlantılarını Listeleme
```bash
ss -t
```

### UDP Bağlantılarını Listeleme
```bash
ss -u
```

### Dinleme Soketlerini Görüntüleme
```bash
ss -l
```

### Bağlantılarla İlişkili Süreçleri Gösterme
```bash
ss -p
```

### Sayısal Adres ve Port Numaralarıyla Listeleme
```bash
ss -n
```

## Tips
- `ss` komutunu kullanarak ağ sorunlarını hızlı bir şekilde teşhis edebilirsiniz.
- Özellikle `-p` seçeneği ile hangi süreçlerin hangi bağlantıları kullandığını görebilirsiniz; bu, güvenlik ve performans analizi için faydalıdır.
- `ss` komutunu sıkça kullanıyorsanız, belirli bir filtreleme yaparak çıktıyı daha okunabilir hale getirebilirsiniz. Örneğin, belirli bir portu dinleyen bağlantıları görmek için `ss -ltn 'sport = :80'` komutunu kullanabilirsiniz.