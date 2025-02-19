# [Linux] C Shell (csh) tr Kullanımı: Karakterleri Dönüştürme

## Overview
`tr` komutu, bir dosyadaki veya standart girdi akışındaki karakterleri dönüştürmek veya silmek için kullanılır. Bu komut, metin işleme işlemlerinde oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
tr [options] [arguments]
```

## Common Options
- `-d`: Belirtilen karakterleri siler.
- `-s`: Ardışık aynı karakterleri tek bir karakterle birleştirir.
- `-c`: Belirtilen karakterler dışındaki tüm karakterleri işler.
- `-t`: Belirtilen karakterleri hedef karakterlerle değiştirir.

## Common Examples
Aşağıda `tr` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Karakter Dönüştürme**
   Büyük harfleri küçük harflere dönüştürmek için:
   ```csh
   echo "HELLO WORLD" | tr 'A-Z' 'a-z'
   ```

2. **Karakter Silme**
   Belirli karakterleri silmek için:
   ```csh
   echo "Hello, World!" | tr -d 'o'
   ```

3. **Ardışık Karakterleri Birleştirme**
   Ardışık boşlukları tek bir boşlukla birleştirmek için:
   ```csh
   echo "Hello    World!" | tr -s ' '
   ```

4. **Karakterleri Değiştirme**
   Belirli karakterleri başka karakterlerle değiştirmek için:
   ```csh
   echo "apple" | tr 'aeiou' 'AEIOU'
   ```

## Tips
- `tr` komutunu kullanırken, girdi verisinin doğru formatta olduğundan emin olun.
- Birden fazla karakter dönüştürmesi yapacaksanız, dönüşüm dizilerini sıralı olarak belirtin.
- `tr` komutunu bir dosya ile kullanmak için, dosya içeriğini `cat` komutuyla `tr`'ye yönlendirebilirsiniz. Örneğin:
  ```csh
  cat dosya.txt | tr 'a-z' 'A-Z'
  ```