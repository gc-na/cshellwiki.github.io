# [Linux] Bash vmstat Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
`vmstat` komutu, sistemin bellek, işlemci ve I/O (giriş/çıkış) durumunu izlemek için kullanılır. Bu komut, sistem performansını değerlendirmek ve sorunları teşhis etmek için yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
vmstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bellek alanlarını gösterir.
- `-m`: Bellek sayfalarının istatistiklerini gösterir.
- `-s`: Bellek istatistiklerini tablo halinde gösterir.
- `-d`: Disk istatistiklerini gösterir.
- `-t`: Zaman damgası ekler.

## Yaygın Örnekler
1. Sistem durumunu 5 saniye aralıklarla görüntülemek için:
   ```bash
   vmstat 5
   ```

2. Bellek istatistiklerini detaylı bir şekilde görüntülemek için:
   ```bash
   vmstat -a
   ```

3. Disk istatistiklerini görüntülemek için:
   ```bash
   vmstat -d
   ```

4. Zaman damgası ile birlikte sistem durumunu görüntülemek için:
   ```bash
   vmstat -t 5
   ```

## İpuçları
- `vmstat` çıktısını analiz ederken, sistemin genel performansını değerlendirmek için diğer izleme araçlarıyla birlikte kullanın.
- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanarak verileri kaydedebilirsiniz:
  ```bash
  vmstat 5 > vmstat_output.txt
  ```
- Uzun süreli izleme için `vmstat` komutunu bir arka plan işlemi olarak çalıştırabilirsiniz.