# [Linux] C Shell (csh) if Kullanımı: Koşullu ifadeleri değerlendirme

## Overview
`if` komutu, belirli bir koşulun doğru olup olmadığını kontrol etmek için kullanılır. Eğer koşul doğruysa, belirli bir komut veya komut grubu çalıştırılır. Bu, programlama ve betik yazımında karar verme mekanizmaları oluşturmak için oldukça yararlıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
if (koşul) then
    komutlar
endif
```

## Common Options
- `-e`: Dosyanın var olup olmadığını kontrol eder.
- `-d`: Bir dizinin var olup olmadığını kontrol eder.
- `-f`: Bir dosyanın normal bir dosya olup olmadığını kontrol eder.
- `-z`: Bir değişkenin boş olup olmadığını kontrol eder.

## Common Examples
Aşağıda `if` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Dosyanın varlığını kontrol etme
```csh
if (-e dosya.txt) then
    echo "dosya.txt mevcut."
endif
```

### Örnek 2: Boş bir değişken kontrolü
```csh
set myVar = ""
if ("$myVar" == "") then
    echo "Değişken boş."
endif
```

### Örnek 3: Dizin kontrolü
```csh
if (-d /home/kullanici) then
    echo "Kullanıcı dizini mevcut."
endif
```

## Tips
- `if` komutunu kullanırken koşul ifadelerinizi dikkatlice yazın, çünkü yanlış bir ifade beklenmedik sonuçlara yol açabilir.
- Birden fazla koşulu kontrol etmek için `else if` yapısını kullanabilirsiniz.
- Koşul ifadelerinizi parantez içinde yazmayı unutmayın; bu, ifadelerin doğru bir şekilde değerlendirilmesini sağlar.