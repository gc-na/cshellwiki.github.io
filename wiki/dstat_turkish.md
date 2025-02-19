# [Linux] C Shell (csh) dstat Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
dstat, sistem kaynaklarını gerçek zamanlı olarak izlemek için kullanılan bir komuttur. CPU, bellek, disk ve ağ gibi sistem bileşenlerinin performansını takip etmenizi sağlar. Bu sayede sistem yöneticileri ve kullanıcılar, sistemin durumunu daha iyi anlayabilir ve gerektiğinde müdahale edebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
dstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: CPU kullanımını gösterir.
- `-d`: Disk I/O istatistiklerini gösterir.
- `-n`: Ağ trafiğini gösterir.
- `-m`: Bellek kullanımını gösterir.
- `--help`: dstat komutunun yardım menüsünü görüntüler.

## Yaygın Örnekler
Aşağıda dstat komutunun bazı pratik örnekleri verilmiştir:

1. Sadece CPU kullanımını izlemek için:
   ```csh
   dstat -c
   ```

2. Disk I/O ve ağ trafiğini izlemek için:
   ```csh
   dstat -d -n
   ```

3. Tüm sistem kaynaklarını izlemek için:
   ```csh
   dstat
   ```

4. Belirli bir süre boyunca verileri toplamak için (örneğin, her 2 saniyede bir):
   ```csh
   dstat 2
   ```

## İpuçları
- dstat komutunu, sistem performansını analiz etmek için bir izleme aracı olarak kullanın.
- Farklı seçenekleri birleştirerek daha kapsamlı veriler elde edebilirsiniz.
- Uzun süreli izleme için çıktı dosyasına yönlendirme yapabilirsiniz; örneğin: `dstat > output.txt`.