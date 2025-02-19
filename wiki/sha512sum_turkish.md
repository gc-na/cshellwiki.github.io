# [Linux] C Shell (csh) sha512sum Kullanımı: Dosya bütünlüğünü kontrol etme

## Overview
`sha512sum` komutu, dosyaların SHA-512 hash değerlerini hesaplamak için kullanılır. Bu, dosyaların bütünlüğünü kontrol etmek ve veri güvenliğini sağlamak için yaygın bir yöntemdir.

## Usage
Temel sözdizimi şu şekildedir:
```csh
sha512sum [options] [arguments]
```

## Common Options
- `-b`: İkili dosyalar için hash hesaplar.
- `-c`: Hash değerlerini kontrol eder.
- `--tag`: Hash değerini dosya adı ile birlikte gösterir.

## Common Examples
Aşağıda `sha512sum` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosyanın SHA-512 hash değerini hesaplamak:
   ```csh
   sha512sum dosya.txt
   ```

2. Birden fazla dosyanın hash değerlerini hesaplamak:
   ```csh
   sha512sum dosya1.txt dosya2.txt
   ```

3. Bir hash dosyasını kontrol etmek:
   ```csh
   sha512sum -c hash_dosyası.txt
   ```

4. İkili bir dosyanın hash değerini hesaplamak:
   ```csh
   sha512sum -b ikili_dosya.bin
   ```

## Tips
- Hash değerlerini kontrol etmek için, her zaman hash dosyasını güvenilir bir kaynaktan alın.
- Hash değerlerini karşılaştırmadan önce, dosyaların tam olarak aynı olduğundan emin olun.
- `sha512sum` komutunu sık sık kullanıyorsanız, sık kullanılan dosyalar için bir script oluşturmayı düşünebilirsiniz.