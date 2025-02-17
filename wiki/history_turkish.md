# [Linux] Bash history Kullanımı: Komut geçmişini görüntüleme

## Overview
`history` komutu, Bash kabuğunda daha önce çalıştırılan komutların bir listesini görüntülemek için kullanılır. Bu, kullanıcıların geçmişteki komutları hızlı bir şekilde hatırlamasını ve tekrar kullanmasını sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
history [options] [arguments]
```

## Common Options
- `-c`: Geçmişi temizler.
- `-d offset`: Belirtilen konumda (offset) bulunan komutu siler.
- `-a`: Geçmişi dosyaya ekler.
- `-r`: Geçmiş dosyasını okur ve mevcut geçmişe ekler.

## Common Examples
1. Tüm geçmişi görüntüleme:
   ```bash
   history
   ```

2. Geçmişteki son 10 komutu görüntüleme:
   ```bash
   history 10
   ```

3. Belirli bir komutu tekrar çalıştırma (örneğin, 25 numaralı komut):
   ```bash
   !25
   ```

4. Geçmişten belirli bir komutu silme (örneğin, 10 numaralı komut):
   ```bash
   history -d 10
   ```

5. Geçmişi temizleme:
   ```bash
   history -c
   ```

## Tips
- Geçmişteki komutları aramak için `Ctrl + r` tuş kombinasyonunu kullanabilirsiniz.
- Sık kullandığınız komutları bir dosyaya kaydedebilir ve gerektiğinde bu dosyayı okuyarak hızlıca erişebilirsiniz.
- Geçmişi düzenli olarak temizlemek, gereksiz komutların birikmesini önler ve daha düzenli bir çalışma ortamı sağlar.