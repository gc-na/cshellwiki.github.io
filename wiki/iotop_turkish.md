# [Linux] C Shell (csh) iotop Kullanımı: Disk I/O işlemlerini izleme aracı

## Genel Bakış
iotop, sistemdeki disk girdi/çıktı (I/O) işlemlerini izlemek için kullanılan bir komut satırı aracıdır. Bu komut, hangi süreçlerin disk üzerinde ne kadar I/O kaynağı kullandığını gösterir, böylece sistem performansını analiz etmenize yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
iotop [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`, `--only`: Sadece I/O işlemi yapan süreçleri gösterir.
- `-b`, `--batch`: Çıktıyı toplu modda gösterir, bu da komutun arka planda çalıştırılmasına olanak tanır.
- `-n NUM`, `--iter=NUM`: Belirtilen sayıda döngü çalıştırır ve ardından çıkış yapar.
- `-d SEC`, `--delay=SEC`: Her güncelleme arasında beklemek için saniye cinsinden bir süre belirtir.

## Yaygın Örnekler
Aşağıda iotop komutunun bazı pratik örnekleri bulunmaktadır:

1. Temel iotop kullanımı:
   ```bash
   iotop
   ```

2. Sadece I/O işlemi yapan süreçleri görüntülemek için:
   ```bash
   iotop -o
   ```

3. Çıktıyı toplu modda görüntülemek için:
   ```bash
   iotop -b
   ```

4. Her 2 saniyede bir güncelleme yapmak için:
   ```bash
   iotop -d 2
   ```

5. 5 döngü çalıştırmak için:
   ```bash
   iotop -n 5
   ```

## İpuçları
- iotop'u çalıştırmadan önce, komutun doğru çalışabilmesi için root yetkilerine sahip olmanız gerektiğini unutmayın.
- Uzun süreli izleme yapmak istiyorsanız, toplu modda çalıştırarak çıktıyı bir dosyaya yönlendirebilirsiniz:
  ```bash
  iotop -b -n 10 > iotop_output.txt
  ```
- Performans sorunlarını teşhis etmek için iotop'u kullanırken, yüksek I/O kullanımı olan süreçleri not alın ve gerekirse bu süreçleri durdurmayı düşünün.