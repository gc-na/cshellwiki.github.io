# [Linux] Bash mv Kullanımı: Dosya ve dizin taşımak veya yeniden adlandırmak

## Overview
`mv` komutu, dosya ve dizinleri taşımak veya yeniden adlandırmak için kullanılır. Bu komut, belirli bir dosyayı veya dizini yeni bir konuma taşıyabilir veya mevcut bir dosyanın adını değiştirebilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
mv [options] [arguments]
```

## Common Options
- `-i`: Hedef dosya zaten varsa, kullanıcıdan onay ister.
- `-f`: Hedef dosya zaten varsa, onay istemeden üzerine yazar.
- `-u`: Sadece kaynak dosya, hedef dosyadan daha yeni ise taşır.
- `-v`: Taşıma işlemi sırasında hangi dosyaların taşındığını gösterir.

## Common Examples
1. **Dosyayı yeniden adlandırma:**
   ```bash
   mv eski_dosya.txt yeni_dosya.txt
   ```
   Bu komut, `eski_dosya.txt` dosyasını `yeni_dosya.txt` olarak yeniden adlandırır.

2. **Dosyayı başka bir dizine taşıma:**
   ```bash
   mv dosya.txt /hedef/dizin/
   ```
   Bu komut, `dosya.txt` dosyasını `/hedef/dizin/` konumuna taşır.

3. **Birden fazla dosyayı taşıma:**
   ```bash
   mv dosya1.txt dosya2.txt /hedef/dizin/
   ```
   Bu komut, `dosya1.txt` ve `dosya2.txt` dosyalarını belirtilen dizine taşır.

4. **Dosyayı onay isteyerek taşıma:**
   ```bash
   mv -i dosya.txt /hedef/dizin/
   ```
   Bu komut, `dosya.txt` dosyasını taşırken hedef dizinde aynı isimde bir dosya varsa onay ister.

## Tips
- Dosyaları taşımadan önce, hedef dizinin var olduğundan emin olun. Aksi takdirde, `mv` komutu hata verebilir.
- `-v` seçeneğini kullanarak hangi dosyaların taşındığını görmek, işlemi takip etmek için faydalıdır.
- Önemli dosyaları taşırken `-i` seçeneğini kullanarak yanlışlıkla üzerine yazmayı önleyebilirsiniz.