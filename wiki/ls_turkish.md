# [Linux] C Shell (csh) ls Kullanımı: Dosya ve dizinleri listeleme

## Overview
`ls` komutu, mevcut dizindeki dosya ve dizinleri listelemek için kullanılır. Bu komut, dosyaların adlarını, boyutlarını ve diğer özelliklerini görüntülemenizi sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
ls [options] [arguments]
```

## Common Options
- `-l`: Uzun formatta listeleme yapar, dosya izinleri, sahiplik, boyut ve tarih gibi bilgileri gösterir.
- `-a`: Gizli dosyaları da dahil ederek tüm dosyaları listeler.
- `-h`: Boyutları insan tarafından okunabilir formatta gösterir (örneğin, KB, MB).
- `-R`: Alt dizinleri de dahil ederek rekürsif olarak listeleme yapar.
- `-t`: Dosyaları son değiştirilme tarihine göre sıralar.

## Common Examples
Aşağıda `ls` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Temel dosya ve dizin listesini görüntüleme:
   ```csh
   ls
   ```

2. Gizli dosyaları da gösterme:
   ```csh
   ls -a
   ```

3. Uzun formatta listeleme:
   ```csh
   ls -l
   ```

4. Boyutları okunabilir formatta gösterme:
   ```csh
   ls -lh
   ```

5. Alt dizinlerle birlikte listeleme:
   ```csh
   ls -R
   ```

6. Dosyaları son değiştirilme tarihine göre sıralama:
   ```csh
   ls -lt
   ```

## Tips
- `ls` komutunu sık sık kullanıyorsanız, en çok kullandığınız seçenekleri bir alias ile kısayol haline getirebilirsiniz.
- Dizin içeriğini daha iyi anlamak için `-l` ve `-h` seçeneklerini bir arada kullanmak faydalı olabilir.
- Listeleme sonuçlarını bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```csh
  ls -l > dosyalar.txt
  ```