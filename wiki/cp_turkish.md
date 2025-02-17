# [Linux] Bash cp Kullanımı: Dosya ve dizin kopyalama

## Overview
`cp` komutu, Linux ve diğer Unix benzeri işletim sistemlerinde dosya ve dizinleri kopyalamak için kullanılır. Bu komut, kaynak dosyayı belirtilen hedef konuma kopyalar.

## Usage
Temel sözdizimi şu şekildedir:
```
cp [options] [arguments]
```

## Common Options
- `-r`: Dizinleri ve içindeki dosyaları kopyalamak için kullanılır (recursive).
- `-i`: Hedef dosya mevcutsa kullanıcıdan onay ister (interactive).
- `-u`: Sadece kaynak dosya hedef dosyadan daha yeni ise kopyalar (update).
- `-v`: Kopyalama işlemi sırasında hangi dosyaların kopyalandığını gösterir (verbose).
- `-a`: Dosyaların tüm özelliklerini koruyarak kopyalar (archive).

## Common Examples
1. Basit bir dosya kopyalama:
   ```bash
   cp dosya.txt yedek_dosya.txt
   ```

2. Bir dizini ve içindeki tüm dosyaları kopyalama:
   ```bash
   cp -r dizin_adi/ yedek_dizin/
   ```

3. Hedef dosya mevcutsa onay istemek:
   ```bash
   cp -i dosya.txt yedek_dosya.txt
   ```

4. Sadece daha yeni dosyaları kopyalama:
   ```bash
   cp -u dosya.txt yedek_dosya.txt
   ```

5. Kopyalama işlemi sırasında detaylı bilgi almak:
   ```bash
   cp -v dosya.txt yedek_dosya.txt
   ```

## Tips
- Kopyalama işlemi sırasında dosya izinlerini korumak için `-a` seçeneğini kullanın.
- Dizin kopyalarken `-r` seçeneğini kullanmayı unutmayın, aksi takdirde yalnızca boş dizin kopyalanır.
- Dosyaları kopyalamadan önce hedef dizinin mevcut olduğundan emin olun; aksi takdirde hata alırsınız.