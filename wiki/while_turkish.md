# [Linux] C Shell (csh) while kullanımı: Döngü içinde komut çalıştırma

## Overview
`while` komutu, belirli bir koşul doğru olduğu sürece bir veya daha fazla komutun sürekli olarak çalıştırılmasını sağlar. Bu, döngüsel işlemler gerçekleştirmek için oldukça kullanışlıdır.

## Usage
Temel sözdizimi şu şekildedir:

```csh
while (koşul)
    komutlar
end
```

## Common Options
`while` komutunun kendisi için özel bir seçenek yoktur, ancak döngü içinde kullanılan komutlar için çeşitli seçenekler olabilir. Örneğin, `echo`, `set`, `if` gibi komutlar kullanılabilir.

## Common Examples

### Örnek 1: Basit bir sayaç
```csh
set i = 1
while ($i <= 5)
    echo "Sayaç: $i"
    @ i++
end
```
Bu örnekte, sayaç 1'den 5'e kadar olan sayıları ekrana yazdırır.

### Örnek 2: Kullanıcıdan giriş alma
```csh
set input = ""
while ("$input" != "çıkış")
    echo "Bir şey yazın (çıkış için 'çıkış' yazın):"
    set input = $< 
end
```
Bu örnekte, kullanıcı "çıkış" yazana kadar sürekli olarak giriş alır.

### Örnek 3: Dosya kontrolü
```csh
set filename = "test.txt"
while (! -e $filename)
    echo "$filename bulunamadı, tekrar deniyor..."
    sleep 2
end
echo "$filename bulundu!"
```
Bu örnekte, `test.txt` dosyası bulunana kadar döngü devam eder.

## Tips
- Döngü koşullarını dikkatli belirleyin; sonsuz döngülerden kaçının.
- Döngü içinde kullanılan komutların performansını göz önünde bulundurun.
- Kullanıcıdan giriş alırken, döngünün çıkış koşulunu net bir şekilde belirtin.