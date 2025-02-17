# [Linux] Bash sleep Kullanımı: Bekleme süresi ayarlama

## Overview
`sleep` komutu, belirli bir süre boyunca işlemciyi duraklatmak için kullanılır. Bu, scriptlerde belirli bir süre beklemek gerektiğinde oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
sleep [seçenekler] [süre]
```

## Common Options
- `-s`, `--seconds`: Süreyi saniye cinsinden belirtir. Varsayılan olarak, süre saniye cinsindendir.
- `-m`, `--minutes`: Süreyi dakika cinsinden belirtir.
- `-h`, `--hours`: Süreyi saat cinsinden belirtir.
- `-d`, `--days`: Süreyi gün cinsinden belirtir.

## Common Examples
Aşağıda `sleep` komutunun bazı pratik örnekleri bulunmaktadır:

1. **5 saniye beklemek:**
   ```bash
   sleep 5
   ```

2. **2 dakika beklemek:**
   ```bash
   sleep 2m
   ```

3. **1 saat beklemek:**
   ```bash
   sleep 1h
   ```

4. **3 gün beklemek:**
   ```bash
   sleep 3d
   ```

5. **Bir script içinde bekleme süresi ayarlamak:**
   ```bash
   echo "İşlem başlıyor..."
   sleep 10
   echo "İşlem tamamlandı!"
   ```

## Tips
- `sleep` komutunu, zamanlayıcılar veya döngüler içinde kullanarak scriptlerinizi daha verimli hale getirebilirsiniz.
- Uzun süreli beklemelerde, süreyi gün, saat veya dakika cinsinden belirtmek, komutun okunabilirliğini artırır.
- `sleep` komutunu kullanırken, bekleme süresinin gereksiz yere uzun olmamasına dikkat edin; bu, scriptin genel performansını etkileyebilir.