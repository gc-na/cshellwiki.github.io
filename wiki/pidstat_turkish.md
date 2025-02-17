# [Linux] Bash pidstat Kullanımı: Süreç istatistiklerini görüntüleme

## Overview
`pidstat` komutu, Linux sistemlerinde çalışan süreçlerin istatistiklerini görüntülemek için kullanılır. Bu komut, belirli bir süre boyunca süreçlerin CPU, bellek ve diğer kaynak kullanımlarını izleyerek sistem yöneticilerine yardımcı olur.

## Usage
Temel kullanım sözdizimi aşağıdaki gibidir:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Başlıkları gösterir.
- `-r`: Bellek kullanımı istatistiklerini gösterir.
- `-u`: CPU kullanım istatistiklerini gösterir.
- `-p`: Belirli bir süreç ID'si (PID) için istatistikleri görüntüler.
- `-t`: Tüm alt süreçlerin istatistiklerini gösterir.

## Common Examples
Aşağıda `pidstat` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Tüm süreçlerin CPU kullanımını görüntüleme
```bash
pidstat
```

### 2. Belirli bir PID için CPU ve bellek kullanımını görüntüleme
```bash
pidstat -p 1234
```

### 3. Her 2 saniyede bir CPU kullanımını görüntüleme
```bash
pidstat 2
```

### 4. Bellek kullanımını gösterme
```bash
pidstat -r
```

### 5. Tüm alt süreçlerin istatistiklerini görüntüleme
```bash
pidstat -t
```

## Tips
- `pidstat` komutunu belirli bir süre aralığında çalıştırarak süreçlerin zaman içindeki performansını izleyebilirsiniz.
- Komutun çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanarak verileri kaydedebilirsiniz.
- Süreçlerin performansını analiz etmek için `pidstat` ile birlikte `grep` komutunu kullanarak belirli süreçleri filtreleyebilirsiniz.