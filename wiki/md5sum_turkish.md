# [Linux] C Shell (csh) md5sum Kullanımı: Dosyaların MD5 Hash Değerini Hesaplama

## Overview
md5sum komutu, dosyaların MD5 hash değerlerini hesaplamak için kullanılır. Bu, dosyaların bütünlüğünü kontrol etmek ve dosya karşılaştırmaları yapmak için yaygın olarak kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
md5sum [options] [arguments]
```

## Common Options
- `-b`: İkili dosyalar için kullanılır.
- `-c`: MD5 hash değerlerini kontrol etmek için bir dosya kullanır.
- `-t`: Dosya yerine standart girdi üzerinden hash hesaplar.
- `--help`: Komutun kullanımını gösterir.

## Common Examples
Aşağıda md5sum komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Bir dosyanın MD5 hash değerini hesaplama
```bash
md5sum dosya.txt
```

### 2. Birden fazla dosyanın MD5 hash değerlerini hesaplama
```bash
md5sum dosya1.txt dosya2.txt
```

### 3. MD5 hash değerlerini bir dosyaya yazma
```bash
md5sum dosya.txt > hash_degerleri.txt
```

### 4. Hash değerlerini kontrol etme
Önce bir hash dosyası oluşturun:
```bash
md5sum dosya.txt > dosya.md5
```
Sonra hash değerini kontrol edin:
```bash
md5sum -c dosya.md5
```

## Tips
- Hash değerlerini kontrol etmek için her zaman hash dosyası ile birlikte kullanın.
- İkili dosyalar için `-b` seçeneğini kullanmayı unutmayın.
- Hash değerlerini kaydetmek, dosya bütünlüğünü sağlamak için iyi bir uygulamadır.