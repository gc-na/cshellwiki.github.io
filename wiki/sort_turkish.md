# [Linux] C Shell (csh) sort Kullanımı: Dosya içeriğini sıralama

## Overview
`sort` komutu, metin dosyalarındaki satırları sıralamak için kullanılır. Bu komut, verileri belirli bir düzene göre (alfabetik veya sayısal) sıralayarak daha düzenli bir görünüm sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
sort [options] [arguments]
```

## Common Options
- `-r`: Ters sıralama yapar (büyükten küçüğe).
- `-n`: Sayısal sıralama yapar.
- `-k`: Belirtilen sütuna göre sıralama yapar.
- `-u`: Tekrar eden satırları kaldırarak yalnızca benzersiz satırları gösterir.
- `-o`: Sıralanmış çıktıyı belirtilen dosyaya yazar.

## Common Examples
Aşağıda `sort` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosyayı alfabetik olarak sıralama:
   ```csh
   sort dosya.txt
   ```

2. Bir dosyayı ters sırayla sıralama:
   ```csh
   sort -r dosya.txt
   ```

3. Sayısal sıralama yapmak:
   ```csh
   sort -n sayilar.txt
   ```

4. Belirli bir sütuna göre sıralama (örneğin, ikinci sütun):
   ```csh
   sort -k 2 dosya.txt
   ```

5. Tekrar eden satırları kaldırarak sıralama:
   ```csh
   sort -u dosya.txt
   ```

6. Sıralanmış çıktıyı yeni bir dosyaya yazma:
   ```csh
   sort -o sirali_dosya.txt dosya.txt
   ```

## Tips
- Sıralama işlemini hızlandırmak için büyük dosyalar üzerinde çalışırken `-S` seçeneği ile bellek boyutunu ayarlayabilirsiniz.
- Sıralama işlemi öncesinde dosyanızın yedeğini almak iyi bir uygulamadır.
- Farklı sıralama seçeneklerini bir arada kullanarak daha karmaşık sıralama işlemleri gerçekleştirebilirsiniz.