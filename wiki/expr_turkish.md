# [Linux] C Shell (csh) expr Kullanımı: Matematiksel ifadeleri değerlendirme

## Overview
`expr` komutu, C Shell (csh) ortamında matematiksel ifadeleri değerlendirmek için kullanılır. Bu komut, sayısal hesaplamalar yapmanın yanı sıra, string işlemleri ve mantıksal karşılaştırmalar için de kullanılabilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
expr [options] [arguments]
```

## Common Options
- `+` : Toplama işlemi.
- `-` : Çıkarma işlemi.
- `*` : Çarpma işlemi.
- `/` : Bölme işlemi.
- `%` : Modül alma (kalan).
- `=` : Eşitlik kontrolü.
- `!=` : Eşit olmama kontrolü.

## Common Examples
Aşağıda `expr` komutunun bazı pratik örnekleri bulunmaktadır:

### Toplama
```csh
expr 5 + 3
```
Bu komut, 5 ile 3'ü toplar ve sonuç olarak 8 döner.

### Çıkarma
```csh
expr 10 - 4
```
Bu komut, 10'dan 4'ü çıkarır ve sonuç 6 olur.

### Çarpma
```csh
expr 7 \* 6
```
Bu komut, 7 ile 6'yı çarpar ve sonuç 42'dir. (Dikkat: Çarpma işlemi için `*` karakterinin önüne `\` koymak gerekir.)

### Bölme
```csh
expr 20 / 4
```
Bu komut, 20'yi 4'e böler ve sonuç 5 olur.

### Modül Alma
```csh
expr 10 % 3
```
Bu komut, 10'un 3'e bölümünden kalanı döndürür, yani sonuç 1'dir.

### String Uzunluğu
```csh
expr length "Merhaba"
```
Bu komut, "Merhaba" kelimesinin uzunluğunu döndürür, yani 7.

## Tips
- `expr` komutunu kullanırken, çarpma işlemi için `*` karakterini kaçırmayı unutmayın.
- Hesaplamalar yaparken, sayıları boşluklarla ayırmayı unutmayın.
- `expr` komutu, sadece tam sayılarla çalışır; ondalıklı sayılar için farklı yöntemler kullanmalısınız.