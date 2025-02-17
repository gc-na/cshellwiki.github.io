# [Linux] Bash blkid Kullanımı: Disk ve dosya sistemlerini tanımlama

## Overview
`blkid` komutu, sistemdeki blok aygıtlarının (diskler, bölümler vb.) kimlik bilgilerini ve dosya sistemlerini görüntülemek için kullanılır. Bu komut, aygıtların UUID'lerini, etiketlerini ve dosya sistemlerini hızlı bir şekilde elde etmenizi sağlar.

## Usage
Temel kullanım şekli aşağıdaki gibidir:

```bash
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: Çıktı formatını belirler. Örneğin, `value`, `full`, `list` gibi seçenekler mevcuttur.
- `-s, --match-tag`: Belirli bir etiketle eşleşen bilgileri gösterir.
- `-p, --probe`: Aygıtları sorgulamak için kullanılır.
- `-h, --help`: Komutun kullanımını ve seçeneklerini gösterir.

## Common Examples
Aşağıda `blkid` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Tüm blok aygıtlarını listeleme:
   ```bash
   blkid
   ```

2. Belirli bir aygıtın bilgilerini görüntüleme:
   ```bash
   blkid /dev/sda1
   ```

3. Çıktıyı sadece UUID ile gösterme:
   ```bash
   blkid -o value -s UUID /dev/sda1
   ```

4. Tüm aygıtların dosya sistemlerini listeleme:
   ```bash
   blkid -o list
   ```

## Tips
- `blkid` komutunu `sudo` ile çalıştırmak, bazı aygıtlara erişim izni gerektiren durumlarda faydalı olabilir.
- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  blkid > aygıt_bilgileri.txt
  ```
- UUID'leri kullanarak belirli bir aygıta referans vermek, sistemdeki aygıtların değişkenlik göstermesi durumunda daha güvenilir bir yöntemdir.