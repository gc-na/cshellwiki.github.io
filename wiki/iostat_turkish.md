# [Linux] C Shell (csh) iostat Kullanımı: Sistem girdi/çıktı istatistiklerini görüntüleme

## Overview
`iostat` komutu, sistemin girdi/çıktı (I/O) istatistiklerini izlemek için kullanılır. Bu komut, disklerin performansını değerlendirmek ve sistem üzerindeki I/O yükünü analiz etmek amacıyla yararlıdır.

## Usage
Temel sözdizimi şu şekildedir:
```csh
iostat [options] [arguments]
```

## Common Options
- `-c`: CPU istatistiklerini gösterir.
- `-d`: Disk istatistiklerini gösterir.
- `-x`: Genişletilmiş disk istatistiklerini gösterir.
- `-h`: İnsan tarafından okunabilir formatta çıktı verir.
- `interval`: İstatistiklerin güncellenme aralığını belirtir.

## Common Examples
Aşağıda `iostat` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Temel Disk İstatistiklerini Görüntüleme**
   ```csh
   iostat
   ```

2. **CPU İstatistiklerini Gösterme**
   ```csh
   iostat -c
   ```

3. **Disk İstatistiklerini Belirli Bir Aralıkla Görüntüleme**
   ```csh
   iostat -d 5
   ```

4. **Genişletilmiş Disk İstatistiklerini Görüntüleme**
   ```csh
   iostat -x
   ```

5. **İnsan Okunabilir Formatla Çıktı Alma**
   ```csh
   iostat -h
   ```

## Tips
- `iostat` komutunu düzenli aralıklarla çalıştırarak sistemdeki I/O performansını izleyebilirsiniz.
- Disklerin hangi süreçler tarafından kullanıldığını anlamak için `iostat -x` seçeneğini tercih edin.
- Uzun süreli izleme için çıktıyı bir dosyaya yönlendirebilir ve daha sonra analiz edebilirsiniz:
  ```csh
  iostat -d 5 > iostat_output.txt
  ```