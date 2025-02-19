# [Linux] C Shell (csh) exec Kullanımı: Komutları değiştirme

## Overview
`exec` komutu, mevcut shell oturumunda yeni bir komut çalıştırmak için kullanılır. Bu komut, mevcut shell'i yeni bir programla değiştirir ve bu program çalıştıktan sonra shell geri dönmez.

## Usage
Temel sözdizimi şu şekildedir:
```csh
exec [options] [arguments]
```

## Common Options
- `-a`: Belirtilen programı çalıştırmadan önce alternatif bir isim belirler.
- `-l`: Yeni shell'i oturum açma shell'i olarak başlatır.
- `-c`: Komutları bir dize olarak alır ve çalıştırır.

## Common Examples
1. Basit bir komut çalıştırma:
   ```csh
   exec ls -l
   ```
   Bu komut, mevcut shell'i `ls -l` komutuyla değiştirir ve dosya listesini gösterir.

2. Bir programı alternatif bir isimle çalıştırma:
   ```csh
   exec -a myalias /usr/bin/python3
   ```
   Bu komut, `python3` programını `myalias` adıyla çalıştırır.

3. Bir shell oturumu başlatma:
   ```csh
   exec -l /bin/bash
   ```
   Bu komut, mevcut shell'i `bash` ile değiştirir ve oturum açma shell'i olarak başlatır.

## Tips
- `exec` komutunu kullanırken, mevcut shell oturumunun sona ereceğini unutmayın. Bu nedenle, önemli işlemleri kaydettiğinizden emin olun.
- `exec` ile çalıştırdığınız programın sonlanması durumunda, shell geri dönmeyecektir. Bu yüzden dikkatli kullanın.
- `exec` komutunu, bir script içinde kullanarak, scriptin sonrasında başka bir komut çalıştırmak yerine mevcut shell'i değiştirmek için faydalı hale getirebilirsiniz.