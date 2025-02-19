# [Linux] C Shell (csh) fsck Kullanımı: Dosya sistemini kontrol etme

## Overview
`fsck` (file system check), dosya sistemlerini kontrol etmek ve onarmak için kullanılan bir komuttur. Dosya sistemindeki hataları tespit eder ve düzeltir, bu sayede veri kaybını önlemeye yardımcı olur.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
fsck [options] [arguments]
```

## Common Options
- `-a`: Otomatik onarım yapar. Hataları düzeltmek için kullanıcı müdahalesi gerektirmez.
- `-n`: Dosya sistemini kontrol eder ancak onarım yapmaz. Sadece hataları raporlar.
- `-y`: Tüm hataları otomatik olarak düzeltir. Kullanıcıdan onay istemez.
- `-t`: Belirli bir dosya sisteminin kontrol süresini gösterir.

## Common Examples
Aşağıda `fsck` komutunun bazı pratik örnekleri bulunmaktadır:

1. Tüm dosya sistemlerini kontrol etmek için:
   ```bash
   fsck -A
   ```

2. Belirli bir dosya sistemini kontrol etmek için:
   ```bash
   fsck /dev/sda1
   ```

3. Hataları otomatik olarak düzeltmek için:
   ```bash
   fsck -y /dev/sda1
   ```

4. Sadece hataları raporlamak için:
   ```bash
   fsck -n /dev/sda1
   ```

## Tips
- `fsck` komutunu çalıştırmadan önce dosya sisteminin montajının kaldırıldığından emin olun. Aksi takdirde, veri kaybı riski vardır.
- Düzenli olarak dosya sisteminizi kontrol etmek, potansiyel sorunları erken tespit etmenize yardımcı olabilir.
- Eğer bir dosya sisteminde sürekli hatalarla karşılaşıyorsanız, donanım sorunlarını kontrol etmekte fayda vardır.