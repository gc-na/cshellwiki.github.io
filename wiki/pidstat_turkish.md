# [Linux] C Shell (csh) pidstat Kullanımı: İşlem istatistiklerini görüntüleme

## Genel Bakış
`pidstat` komutu, sistemdeki işlemlerin performans istatistiklerini görüntülemek için kullanılır. Bu komut, belirli bir işlem veya işlemler grubunun CPU, bellek ve diğer kaynak kullanımını izlemeye yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
pidstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Başlıkları gösterir.
- `-r`: Bellek kullanım istatistiklerini gösterir.
- `-u`: CPU kullanım istatistiklerini gösterir.
- `-p <pid>`: Belirtilen işlem kimliğine (PID) göre istatistikleri görüntüler.
- `-t`: Tüm iş parçacıklarının istatistiklerini gösterir.

## Yaygın Örnekler
Aşağıda `pidstat` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm işlemler için CPU kullanımını görüntüleme:
   ```bash
   pidstat -u
   ```

2. Belirli bir PID için bellek kullanımını görüntüleme:
   ```bash
   pidstat -r -p 1234
   ```

3. Her 2 saniyede bir CPU ve bellek kullanımını izleme:
   ```bash
   pidstat -u -r 2
   ```

4. Tüm iş parçacıkları için istatistikleri görüntüleme:
   ```bash
   pidstat -t
   ```

## İpuçları
- `pidstat` komutunu bir betik içinde kullanarak belirli işlemlerin performansını düzenli olarak izleyebilirsiniz.
- İstatistikleri daha iyi analiz etmek için çıktıyı bir dosyaya yönlendirebilirsiniz:
  ```bash
  pidstat -u > istatistikler.txt
  ```
- Uzun süreli izleme için `-h` seçeneğini kullanarak başlıkları görünür tutmayı unutmayın.