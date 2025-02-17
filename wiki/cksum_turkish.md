# [Linux] Bash cksum Kullanımı: Dosya kontrol toplamını hesaplama

## Overview
`cksum` komutu, bir dosyanın kontrol toplamını (checksum) ve byte sayısını hesaplamak için kullanılır. Bu, dosyanın bütünlüğünü doğrulamak veya dosya karşılaştırmaları yapmak için yararlıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm`: Kullanılacak algoritmayı belirtir (örneğin, `md5`, `sha256`).
- `--help`: Komut hakkında yardım bilgisi gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Common Examples
Aşağıda `cksum` komutunun bazı pratik örnekleri bulunmaktadır:

1. Bir dosyanın kontrol toplamını hesaplamak:
   ```bash
   cksum dosya.txt
   ```

2. Birden fazla dosyanın kontrol toplamlarını hesaplamak:
   ```bash
   cksum dosya1.txt dosya2.txt
   ```

3. Kontrol toplamı algoritmasını belirtmek:
   ```bash
   cksum -a md5 dosya.txt
   ```

4. Yardım bilgisi almak:
   ```bash
   cksum --help
   ```

## Tips
- Dosya bütünlüğünü kontrol etmek için `cksum` çıktısını kaydedip daha sonra karşılaştırabilirsiniz.
- Büyük dosyalarla çalışırken, kontrol toplamını hesaplamak zaman alabilir; bu nedenle dosya boyutunu göz önünde bulundurun.
- `cksum` çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  cksum dosya.txt > kontrol_toplami.txt
  ```