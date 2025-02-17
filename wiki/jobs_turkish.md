# [Linux] Bash jobs Kullanımı: Arka planda çalışan işlemleri listeleme

## Overview
`jobs` komutu, Bash kabuğunda arka planda çalışan işlemleri listelemek için kullanılır. Bu komut, kullanıcıya hangi işlemlerin aktif olduğunu ve bunların durumunu gösterir.

## Usage
Temel sözdizimi şu şekildedir:
```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: İşlemlerin PID'lerini (Process ID) gösterir.
- `-n`: Sadece durumu değişen işlemleri listeler.
- `-p`: Sadece işlemlerin PID'lerini gösterir.

## Common Examples
Aşağıda `jobs` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Arka planda çalışan tüm işlemleri listeleme:
   ```bash
   jobs
   ```

2. PID'leri ile birlikte işlemleri listeleme:
   ```bash
   jobs -l
   ```

3. Sadece durumu değişen işlemleri görüntüleme:
   ```bash
   jobs -n
   ```

4. Sadece işlemlerin PID'lerini gösterme:
   ```bash
   jobs -p
   ```

## Tips
- `jobs` komutunu kullanmadan önce arka planda bir işlem başlatmayı unutmayın. Örneğin, bir komutu `&` ile sonlandırarak arka plana alabilirsiniz.
- `fg` komutunu kullanarak arka planda çalışan bir işlemi ön plana alabilirsiniz.
- `bg` komutunu kullanarak duraklatılmış bir işlemi arka planda devam ettirebilirsiniz.