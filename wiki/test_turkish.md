# [Linux] C Shell (csh) test Kullanımı: Koşul ifadelerini değerlendirme

## Overview
`test` komutu, bir koşul ifadesini değerlendirerek, belirtilen koşulun doğru (true) veya yanlış (false) olduğunu belirler. Bu komut, genellikle betiklerde koşullu ifadeleri kontrol etmek için kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
test [options] [arguments]
```

## Common Options
- `-e [dosya]`: Belirtilen dosyanın var olup olmadığını kontrol eder.
- `-d [dosya]`: Belirtilen dosyanın bir dizin olup olmadığını kontrol eder.
- `-f [dosya]`: Belirtilen dosyanın bir dosya olup olmadığını kontrol eder.
- `-z [string]`: Belirtilen string'in boş olup olmadığını kontrol eder.
- `-n [string]`: Belirtilen string'in boş olmadığını kontrol eder.

## Common Examples
Aşağıda `test` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Dosyanın varlığını kontrol etme
```csh
test -e dosya.txt && echo "Dosya mevcut."
```

### 2. Dizin kontrolü
```csh
test -d /home/kullanici && echo "Bu bir dizin."
```

### 3. Dosya kontrolü
```csh
test -f /etc/passwd && echo "Bu bir dosya."
```

### 4. Boş string kontrolü
```csh
string=""
test -z "$string" && echo "String boş."
```

### 5. Boş olmayan string kontrolü
```csh
string="Merhaba"
test -n "$string" && echo "String boş değil."
```

## Tips
- `test` komutunu kullanırken, koşul ifadelerinizi parantez içinde yazmak, karmaşık koşulları daha okunabilir hale getirebilir.
- `test` komutunun yerine `[` veya `[[` kullanarak da benzer işlemleri gerçekleştirebilirsiniz; bu, bazı durumlarda daha fazla seçenek sunabilir.
- Koşul ifadelerinizi bir betik içinde kullanırken, `if` yapısını kullanarak daha iyi kontrol akışı sağlayabilirsiniz.