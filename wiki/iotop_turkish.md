# [Linux] Bash iotop Kullanımı: Disk I/O İzleme Aracı

## Genel Bakış
iotop, Linux sistemlerinde disk girdi/çıktı (I/O) işlemlerini izlemek için kullanılan bir komut satırı aracıdır. Bu araç, hangi süreçlerin disk üzerinde ne kadar I/O yaptığını göstererek sistem yöneticilerine ve kullanıcılarına sistem performansını analiz etme imkanı sunar.

## Kullanım
Temel kullanım senaryosu aşağıdaki gibidir:

```bash
iotop [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`, `--only`: Sadece I/O işlemi yapan süreçleri gösterir.
- `-b`, `--batch`: Çıktıyı toplu modda gösterir, bu sayede çıktıyı bir dosyaya yönlendirmek mümkündür.
- `-n NUM`, `--iter=NUM`: Belirtilen sayıda döngü gerçekleştirilmesini sağlar.
- `-d SEC`, `--delay=SEC`: Her güncelleme arasında bekleme süresini (saniye cinsinden) ayarlar.

## Yaygın Örnekler
Aşağıda iotop komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Temel Kullanım:**
   ```bash
   iotop
   ```
   Bu komut, anlık olarak disk I/O işlemlerini gösterir.

2. **Sadece I/O Yapan Süreçleri Gösterme:**
   ```bash
   iotop -o
   ```
   Bu komut, yalnızca disk üzerinde I/O işlemi gerçekleştiren süreçleri listeler.

3. **Toplu Modda Çalıştırma:**
   ```bash
   iotop -b -n 5
   ```
   Bu komut, 5 döngü boyunca toplu modda I/O bilgilerini gösterir.

4. **Güncelleme Aralığını Ayarlama:**
   ```bash
   iotop -d 2
   ```
   Bu komut, her 2 saniyede bir güncellemeleri gösterir.

## İpuçları
- iotop'u çalıştırmak için genellikle root yetkilerine ihtiyaç duyarsınız. Bu nedenle `sudo` ile çalıştırmayı unutmayın.
- Uzun süreli izleme yapacaksanız, çıktıyı bir dosyaya yönlendirmek için `-b` seçeneğini kullanarak verileri kaydedebilirsiniz.
- Performans sorunlarını analiz ederken, hangi süreçlerin en fazla I/O yaptığını belirlemek için `-o` seçeneğini kullanmak faydalı olacaktır.