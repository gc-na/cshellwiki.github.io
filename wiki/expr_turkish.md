# [Linux] Bash expr Kullanımı: Matematiksel ve Mantıksal Hesaplamalar

## Overview
`expr` komutu, Bash ortamında matematiksel ve mantıksal hesaplamalar yapmak için kullanılan bir araçtır. Temel olarak, sayılar üzerinde işlemler gerçekleştirebilir ve string manipülasyonları yapabilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
expr [options] [arguments]
```

## Common Options
- `+` : Toplama işlemi.
- `-` : Çıkarma işlemi.
- `*` : Çarpma işlemi. (Dikkat: Çarpma işlemi için `\*` şeklinde yazılmalıdır.)
- `/` : Bölme işlemi.
- `%` : Modül (kalan) işlemi.
- `=` : Eşitlik kontrolü.
- `!=` : Eşit olmama kontrolü.

## Common Examples
Aşağıda `expr` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Toplama
```bash
expr 5 + 3
```
Bu komut, 5 ile 3'ü toplar ve sonucu 8 olarak döndürür.

### Çıkarma
```bash
expr 10 - 4
```
Bu komut, 10'dan 4'ü çıkarır ve sonucu 6 olarak döndürür.

### Çarpma
```bash
expr 4 \* 2
```
Bu komut, 4 ile 2'yi çarpar ve sonucu 8 olarak döndürür.

### Bölme
```bash
expr 20 / 4
```
Bu komut, 20'yi 4'e böler ve sonucu 5 olarak döndürür.

### Modül
```bash
expr 10 % 3
```
Bu komut, 10'un 3'e bölümünden kalanını hesaplar ve sonucu 1 olarak döndürür.

### String Uzunluğu
```bash
expr length "Merhaba"
```
Bu komut, "Merhaba" kelimesinin uzunluğunu döndürür ve sonucu 7 olarak verir.

## Tips
- `expr` komutunu kullanırken, çarpma işlemi için `\*` kullanmayı unutmayın; aksi takdirde hata alırsınız.
- Daha karmaşık işlemler için parantez kullanarak öncelik sıralaması oluşturabilirsiniz.
- `expr` komutunun çıktısını bir değişkene atamak için `$(...)` veya `` `...` `` kullanabilirsiniz. Örneğin:
  ```bash
  sonuc=$(expr 5 + 3)
  echo $sonuc
  ```
- `expr` komutu, sadece sayılarla değil, aynı zamanda stringlerle de çalışabilir; bu nedenle metin işlemleri için de kullanılabilir.