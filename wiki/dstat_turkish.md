# [Linux] Bash dstat Kullanımı: Sistem kaynaklarını izleme aracı

## Overview
dstat, sistem kaynaklarını gerçek zamanlı olarak izlemek için kullanılan bir komut satırı aracıdır. CPU, disk, ağ ve bellek gibi sistem bileşenlerinin performansını izlemek için kullanılır. dstat, sistem yöneticileri ve geliştiriciler için yararlı bir araçtır, çünkü sistemin durumunu anlık olarak gözlemlemeye olanak tanır.

## Usage
dstat komutunun temel sözdizimi aşağıdaki gibidir:

```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: CPU kullanımını gösterir.
- `-d`: Disk I/O istatistiklerini gösterir.
- `-n`: Ağ istatistiklerini gösterir.
- `-m`: Bellek kullanımını gösterir.
- `-t`: Zaman damgası ekler.
- `--help`: dstat komutunun yardım sayfasını gösterir.

## Common Examples
Aşağıda dstat komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Sadece CPU ve bellek kullanımını izlemek için:
   ```bash
   dstat -c -m
   ```

2. Disk ve ağ istatistiklerini izlemek için:
   ```bash
   dstat -d -n
   ```

3. Tüm istatistikleri zaman damgası ile birlikte izlemek için:
   ```bash
   dstat -t
   ```

4. Belirli bir süre boyunca (örneğin, 10 saniye) izlemek için:
   ```bash
   dstat 10
   ```

## Tips
- dstat'ı kullanırken, hangi kaynakların izlenmesi gerektiğini belirlemek için sistemin ihtiyaçlarını göz önünde bulundurun.
- Uzun süreli izleme yapacaksanız, çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  dstat -c -d > istatistikler.txt
  ```
- dstat'ı diğer komutlarla birleştirerek daha kapsamlı analizler yapabilirsiniz. Örneğin, `grep` ile belirli bir çıktıyı filtreleyebilirsiniz.