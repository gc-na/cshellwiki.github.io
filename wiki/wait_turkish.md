# [Linux] Bash wait Kullanımı: İşlem bekletme komutu

## Overview
`wait` komutu, bir veya daha fazla arka plan işleminin tamamlanmasını beklemek için kullanılır. Bu komut, özellikle birden fazla işlemi aynı anda yürütürken, belirli bir işlemin bitmesini beklemek için faydalıdır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Bekleyen ilk tamamlanan işlemi bekler.
- `PID`: Belirtilen işlem kimliğine (PID) sahip olan işlemi bekler. Eğer PID verilmezse, tüm arka plan işlemleri beklenir.

## Common Examples
1. **Tüm arka plan işlemlerini beklemek:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "Tüm işlemler tamamlandı."
   ```

2. **Belirli bir PID'yi beklemek:**
   ```bash
   sleep 5 &
   PID=$!
   echo "PID: $PID"
   wait $PID
   echo "Belirtilen işlem tamamlandı."
   ```

3. **İlk tamamlanan işlemi beklemek:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait -n
   echo "İlk tamamlanan işlem sona erdi."
   ```

## Tips
- `wait` komutunu kullanmadan önce işlemlerin arka planda çalıştığından emin olun.
- Birden fazla işlem başlatırken, her birinin PID'sini kaydedip, bunları beklemek için kullanabilirsiniz.
- `wait` komutunu bir betikte kullanarak, işlemlerin sıralı bir şekilde tamamlanmasını sağlayabilirsiniz.