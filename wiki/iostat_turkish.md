# [Linux] Bash iostat Kullanımı: Disk ve CPU istatistiklerini görüntüleme

## Overview
`iostat` komutu, sistemin giriş/çıkış (I/O) istatistiklerini ve CPU kullanımını izlemek için kullanılır. Bu komut, disklerin ve diğer I/O aygıtlarının performansını değerlendirmeye yardımcı olur.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
iostat [options] [arguments]
```

## Common Options
- `-c`: Sadece CPU istatistiklerini gösterir.
- `-d`: Sadece disk istatistiklerini gösterir.
- `-x`: Genişletilmiş disk istatistiklerini gösterir.
- `-m`: Çıktıyı megabayt cinsinden gösterir.
- `-t`: Zaman damgası ile birlikte çıktı verir.

## Common Examples
Aşağıda `iostat` komutunun bazı pratik örnekleri verilmiştir:

1. Temel disk ve CPU istatistiklerini görüntüleme:
   ```bash
   iostat
   ```

2. Sadece CPU istatistiklerini görüntüleme:
   ```bash
   iostat -c
   ```

3. Disk istatistiklerini genişletilmiş formatta görüntüleme:
   ```bash
   iostat -x
   ```

4. Çıktıyı megabayt cinsinden görüntüleme:
   ```bash
   iostat -m
   ```

5. Belirli bir süre aralığında istatistikleri görüntüleme (örneğin, her 5 saniyede bir):
   ```bash
   iostat 5
   ```

## Tips
- `iostat` komutunu düzenli olarak kullanarak sisteminizin performansını izleyin.
- Disk performansındaki düşüşleri belirlemek için `-x` seçeneği ile detaylı istatistikleri inceleyin.
- Uzun süreli izleme için çıktıyı bir dosyaya yönlendirin:
  ```bash
  iostat -x 5 > iostat_output.txt
  ```