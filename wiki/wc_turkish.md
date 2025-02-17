# [Linux] Bash wc Kullanımı: Dosya içeriğindeki satır, kelime ve byte sayısını hesaplar

## Overview
`wc` (word count), bir dosyanın içeriğindeki satır, kelime ve byte sayısını hesaplamak için kullanılan bir Bash komutudur. Bu komut, metin dosyalarının analizinde ve içeriklerinin hızlı bir şekilde özetlenmesinde oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
wc [options] [arguments]
```

## Common Options
- `-l`: Sadece satır sayısını gösterir.
- `-w`: Sadece kelime sayısını gösterir.
- `-c`: Sadece byte sayısını gösterir.
- `-m`: Sadece karakter sayısını gösterir.
- `-L`: En uzun satırın uzunluğunu gösterir.

## Common Examples
Aşağıda `wc` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosyanın satır, kelime ve byte sayısını görüntülemek:
   ```bash
   wc dosya.txt
   ```

2. Sadece satır sayısını almak:
   ```bash
   wc -l dosya.txt
   ```

3. Sadece kelime sayısını almak:
   ```bash
   wc -w dosya.txt
   ```

4. Sadece byte sayısını almak:
   ```bash
   wc -c dosya.txt
   ```

5. Birden fazla dosyanın satır, kelime ve byte sayısını görüntülemek:
   ```bash
   wc dosya1.txt dosya2.txt
   ```

## Tips
- `wc` komutunu diğer komutlarla birleştirerek daha karmaşık analizler yapabilirsiniz. Örneğin, `grep` ile belirli bir kelimeyi içeren satırları sayabilirsiniz:
  ```bash
  grep "kelime" dosya.txt | wc -l
  ```
- Dosya içeriğini incelemeden önce `wc` komutunu kullanarak dosyanın büyüklüğünü hızlıca öğrenebilirsiniz.
- `wc` komutunu bir dosya yerine standart girdi ile de kullanabilirsiniz. Örneğin, bir metni doğrudan terminalden girerek kelime sayısını öğrenmek için:
  ```bash
  echo "Bu bir test metnidir." | wc -w
  ```