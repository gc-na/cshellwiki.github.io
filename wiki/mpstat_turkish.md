# [Linux] C Shell (csh) mpstat Kullanımı: CPU istatistiklerini görüntüleme

## Genel Bakış
mpstat komutu, sistemdeki CPU kullanım istatistiklerini görüntülemek için kullanılır. Bu komut, her bir CPU'nun yükünü ve performansını analiz etmek için faydalıdır.

## Kullanım
mpstat komutunun temel sözdizimi aşağıdaki gibidir:

```csh
mpstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-P ALL`: Tüm CPU'ların istatistiklerini gösterir.
- `-u`: Kullanıcı ve sistem CPU kullanım yüzdelerini görüntüler.
- `-h`: Çıktıyı daha okunabilir hale getirir.
- `interval`: İstatistiklerin güncellenme aralığını saniye cinsinden belirtir.
- `count`: İstatistiklerin kaç kez gösterileceğini belirtir.

## Yaygın Örnekler
Aşağıda mpstat komutunun bazı pratik örnekleri verilmiştir:

1. Tüm CPU'ların istatistiklerini görüntülemek için:
   ```csh
   mpstat -P ALL
   ```

2. Kullanıcı ve sistem CPU kullanım yüzdelerini görüntülemek için:
   ```csh
   mpstat -u
   ```

3. Her 2 saniyede bir CPU istatistiklerini güncellemek için (5 kez):
   ```csh
   mpstat 2 5
   ```

4. Daha okunabilir bir çıktı almak için:
   ```csh
   mpstat -h
   ```

## İpuçları
- mpstat komutunu, sistem performansını izlemek için düzenli aralıklarla çalıştırarak sistemdeki darboğazları tespit edebilirsiniz.
- Çıktıyı bir dosyaya yönlendirerek, zaman içinde CPU kullanımını analiz etmek için verileri kaydedebilirsiniz:
  ```csh
  mpstat -P ALL 2 5 > cpu_istatistikleri.txt
  ```
- Özellikle yoğun yük altında çalışan sistemlerde, CPU kullanımını izlemek için mpstat'ı kullanmak, performans sorunlarını hızlı bir şekilde tanımlamanıza yardımcı olabilir.