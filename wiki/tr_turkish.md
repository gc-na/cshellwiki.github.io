# [Linux] Bash tr Kullanımı: Karakterleri Dönüştürme

## Overview
`tr` komutu, bir dosyadaki veya standart girdi akışındaki karakterleri dönüştürmek veya silmek için kullanılır. Genellikle metin işleme görevlerinde, belirli karakterleri değiştirmek veya kaldırmak için oldukça faydalıdır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
tr [seçenekler] [argümanlar]
```

## Common Options
- `-d`: Belirtilen karakterleri siler.
- `-s`: Ardışık aynı karakterleri tek bir karakterle birleştirir.
- `-c`: Belirtilen karakterler dışındaki tüm karakterleri işler.
- `-t`: Belirtilen karakterleri belirli bir karakterle değiştirir.

## Common Examples
Aşağıda `tr` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Karakter Dönüştürme**: Küçük harfleri büyük harflere dönüştürme.
   ```bash
   echo "merhaba dünya" | tr 'a-z' 'A-Z'
   ```

2. **Karakter Silme**: Belirli karakterleri silme.
   ```bash
   echo "merhaba dünya" | tr -d 'a'
   ```

3. **Aynı Karakterleri Sıkıştırma**: Ardışık boşlukları tek bir boşlukla değiştirme.
   ```bash
   echo "merhaba    dünya" | tr -s ' '
   ```

4. **Karakter Değiştirme**: Sayıları harflerle değiştirme.
   ```bash
   echo "1 2 3" | tr '123' 'abc'
   ```

## Tips
- `tr` komutunu kullanmadan önce, hangi karakterleri değiştirmek veya silmek istediğinizi net bir şekilde belirleyin.
- Büyük/küçük harf dönüşümleri için `tr` komutunu kullanırken, dönüşüm tablosunu dikkatlice oluşturun.
- `tr` komutunu bir dosya üzerinde çalıştırmak için, dosya içeriğini `cat` komutuyla `tr`'ye yönlendirebilirsiniz. Örneğin:
  ```bash
  cat dosya.txt | tr 'a-z' 'A-Z'
  ```