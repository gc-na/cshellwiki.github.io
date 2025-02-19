# [Linux] C Shell (csh) watch Kullanımı: Komutların sürekli izlenmesi

## Overview
`watch` komutu, belirli bir komutu belirli aralıklarla çalıştırarak çıktısını sürekli olarak izlemeye yarar. Bu, sistem durumunu veya belirli bir işlemi takip etmek için oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```csh
watch [options] [arguments]
```

## Common Options
- `-n <saniye>`: Komutun her ne kadar sürede bir çalıştırılacağını belirtir. Varsayılan olarak 2 saniyedir.
- `-d`: Çıktıdaki değişiklikleri vurgular. Bu, hangi bilgilerin değiştiğini hızlıca görmenizi sağlar.
- `-t`: Başlık satırını gizler. Çıktıyı daha temiz hale getirir.

## Common Examples
Aşağıda `watch` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Sistemin durumunu izlemek:**
   ```csh
   watch -n 5 uptime
   ```
   Bu komut, her 5 saniyede bir sistemin çalışma süresini gösterir.

2. **Disk kullanımını kontrol etmek:**
   ```csh
   watch -d df -h
   ```
   Bu komut, disk kullanımını her 2 saniyede bir güncelleyerek değişiklikleri vurgular.

3. **Belirli bir dizindeki dosyaları izlemek:**
   ```csh
   watch ls -l /path/to/directory
   ```
   Bu komut, belirtilen dizindeki dosyaların listesini sürekli olarak günceller.

4. **Ağ bağlantı durumunu kontrol etmek:**
   ```csh
   watch -n 10 ping -c 1 google.com
   ```
   Bu komut, her 10 saniyede bir Google'a ping atarak bağlantı durumunu kontrol eder.

## Tips
- `watch` komutunu kullanırken, çok sık güncellemeler yapmaktan kaçının; bu, sistem kaynaklarını gereksiz yere tüketebilir.
- Çıktıyı daha okunabilir hale getirmek için `-d` seçeneğini kullanarak değişiklikleri vurgulayabilirsiniz.
- Komutun çıktısını kaydetmek isterseniz, `tee` komutunu kullanarak çıktıyı bir dosyaya yönlendirebilirsiniz.