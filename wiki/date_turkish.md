# [Linux] C Shell (csh) date Kullanımı: Tarih ve saat bilgisi gösterir

## Overview
`date` komutu, sistemin tarih ve saat bilgilerini görüntülemek için kullanılır. Bu komut, kullanıcıların mevcut tarih ve saat bilgilerini kolayca görmelerini sağlar.

## Usage
Temel sözdizimi şu şekildedir:

```csh
date [options] [arguments]
```

## Common Options
- `+FORMAT`: Tarih ve saat çıktısını belirli bir formatta gösterir.
- `-u`: UTC (Evrensel Koordinat Zamanı) cinsinden tarih ve saat bilgisi gösterir.
- `-d STRING`: Belirtilen STRING ifadesine göre tarih ve saat bilgisi gösterir.

## Common Examples
Aşağıda `date` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Mevcut tarih ve saati görüntüleme:
   ```csh
   date
   ```

2. Tarih ve saati belirli bir formatta gösterme (örneğin, YYYY-AA-GG):
   ```csh
   date +%Y-%m-%d
   ```

3. UTC cinsinden tarih ve saat bilgisi gösterme:
   ```csh
   date -u
   ```

4. Belirli bir tarih ve saat bilgisi gösterme (örneğin, "2023-12-25" tarihi için):
   ```csh
   date -d "2023-12-25"
   ```

## Tips
- Tarih ve saat formatını özelleştirmek için `+FORMAT` seçeneğini kullanarak istediğiniz biçimi elde edebilirsiniz.
- UTC zamanını kullanmak, farklı zaman dilimlerinde çalışan sistemler için faydalıdır.
- Tarih ve saat bilgilerini betiklerde kullanmak için `date` komutunu değişkenlere atayabilirsiniz. Örneğin:
  ```csh
  set current_date = `date +%Y-%m-%d`
  ```