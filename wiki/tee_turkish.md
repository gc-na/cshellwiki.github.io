# [Linux] C Shell (csh) tee Kullanımı: Verileri dosyaya ve ekrana yazma

## Overview
`tee` komutu, standart girdi verilerini hem ekrana hem de bir veya daha fazla dosyaya yazmak için kullanılır. Bu, verileri anlık olarak görüntülemenizi ve aynı zamanda dosyaya kaydetmenizi sağlar.

## Usage
Temel sözdizimi şu şekildedir:
```csh
tee [options] [arguments]
```

## Common Options
- `-a`: Dosyaya ekleme yapar, yani mevcut içeriğin üzerine yazmak yerine yeni verileri ekler.
- `-i`: Girdi akışını keser, yani sinyal yakalamayı devre dışı bırakır.

## Common Examples
Aşağıda `tee` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Temel Kullanım**: Bir dosyaya yazarken aynı zamanda ekrana yazdırma.
   ```csh
   echo "Merhaba Dünya" | tee dosya.txt
   ```

2. **Dosyaya Ekleyerek Yazma**: Mevcut dosya içeriğinin üzerine yazmadan ekleme yapma.
   ```csh
   echo "Yeni Satır" | tee -a dosya.txt
   ```

3. **Birden Fazla Dosyaya Yazma**: Veriyi birden fazla dosyaya aynı anda yazma.
   ```csh
   echo "Veri" | tee dosya1.txt dosya2.txt
   ```

4. **Girdi Akışını Kesme**: Sinyal yakalamayı devre dışı bırakma.
   ```csh
   echo "Önemli Veri" | tee -i dosya.txt
   ```

## Tips
- `tee` komutunu kullanırken, dosya adlarını belirtirken dikkatli olun; yanlış dosya adları mevcut verilerinizi kaybetmenize neden olabilir.
- `-a` seçeneğini kullanarak, verilerinizi kaybetmeden dosyaya ekleme yapabilirsiniz.
- `tee` komutunu, uzun komut dizilerini daha okunabilir hale getirmek için boru (pipe) ile birleştirerek kullanabilirsiniz.