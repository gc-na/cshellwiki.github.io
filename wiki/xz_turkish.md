# [Linux] Bash xz Kullanımı: Dosyaları sıkıştırma ve açma aracı

## Genel Bakış
`xz` komutu, dosyaları sıkıştırmak ve açmak için kullanılan bir araçtır. Yüksek sıkıştırma oranları sunarak disk alanından tasarruf sağlar ve dosyaların daha hızlı aktarımını mümkün kılar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
xz [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-d` veya `--decompress`: Sıkıştırılmış bir dosyayı açar.
- `-k` veya `--keep`: Sıkıştırma işlemi sırasında orijinal dosyayı korur.
- `-f` veya `--force`: Zaten var olan dosyaların üzerine yazılmasını sağlar.
- `-9`: En yüksek sıkıştırma seviyesini kullanır.
- `-t`: Sıkıştırılmış dosyanın doğruluğunu kontrol eder.

## Yaygın Örnekler
1. Bir dosyayı sıkıştırmak:
   ```bash
   xz dosya.txt
   ```
   Bu komut, `dosya.txt` dosyasını sıkıştırarak `dosya.txt.xz` oluşturur.

2. Sıkıştırılmış bir dosyayı açmak:
   ```bash
   xz -d dosya.txt.xz
   ```
   Bu komut, `dosya.txt.xz` dosyasını açarak orijinal `dosya.txt` dosyasını geri getirir.

3. Orijinal dosyayı koruyarak sıkıştırmak:
   ```bash
   xz -k dosya.txt
   ```
   Bu komut, `dosya.txt` dosyasını sıkıştırırken orijinal dosyayı da korur.

4. En yüksek sıkıştırma seviyesini kullanarak sıkıştırmak:
   ```bash
   xz -9 dosya.txt
   ```
   Bu komut, `dosya.txt` dosyasını en yüksek sıkıştırma oranıyla sıkıştırır.

5. Sıkıştırılmış dosyanın doğruluğunu kontrol etmek:
   ```bash
   xz -t dosya.txt.xz
   ```
   Bu komut, `dosya.txt.xz` dosyasının bozulup bozulmadığını kontrol eder.

## İpuçları
- Sıkıştırma işlemi sırasında dosya boyutunu ve işlem süresini dengelemek için farklı sıkıştırma seviyelerini deneyin.
- Büyük dosyalarla çalışırken, sıkıştırma işleminin zaman alabileceğini unutmayın; bu nedenle, işlemi arka planda çalıştırmayı düşünebilirsiniz.
- Sıkıştırılmış dosyaları düzenli olarak kontrol edin, böylece dosya bütünlüğünü sağlarsınız.