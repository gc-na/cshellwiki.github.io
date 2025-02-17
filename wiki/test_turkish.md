# [Linux] Bash test Kullanımı: Koşul testleri yapma

## Genel Bakış
`test` komutu, belirli koşulları kontrol etmek için kullanılan bir Bash komutudur. Dosya varlığı, dosya türü, karşılaştırmalar gibi çeşitli koşulları test etmek için kullanılır. Bu komut, genellikle if ifadeleriyle birlikte kullanılarak, program akışını kontrol etmekte yardımcı olur.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
test [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Belirtilen dosyanın var olup olmadığını kontrol eder.
- `-f`: Belirtilen dosyanın bir dosya olup olmadığını kontrol eder.
- `-d`: Belirtilen yolun bir dizin olup olmadığını kontrol eder.
- `-z`: Belirtilen stringin boş olup olmadığını kontrol eder.
- `=`: İki stringin eşit olup olmadığını kontrol eder.
- `-lt`: İlk sayının ikinci sayıdan küçük olup olmadığını kontrol eder.

## Yaygın Örnekler

### Dosya Varlığını Kontrol Etme
```bash
if test -e dosya.txt; then
    echo "dosya.txt mevcut."
else
    echo "dosya.txt mevcut değil."
fi
```

### Bir Dizinin Var Olup Olmadığını Kontrol Etme
```bash
if test -d /home/kullanici; then
    echo "Dizin mevcut."
else
    echo "Dizin mevcut değil."
fi
```

### String Karşılaştırması
```bash
string1="merhaba"
string2="merhaba"

if test "$string1" = "$string2"; then
    echo "Stringler eşit."
else
    echo "Stringler eşit değil."
fi
```

### Sayı Karşılaştırması
```bash
sayi1=5
sayi2=10

if test $sayi1 -lt $sayi2; then
    echo "$sayi1, $sayi2'den küçüktür."
else
    echo "$sayi1, $sayi2'den küçük değildir."
fi
```

## İpuçları
- `test` komutunu kullanırken, koşulları daha okunabilir hale getirmek için köşeli parantezler `[ ]` kullanabilirsiniz. Örneğin, `if [ -e dosya.txt ]; then`.
- Koşul ifadelerinde boşluklara dikkat edin; yanlış yerleştirilen boşluklar hatalara neden olabilir.
- `test` yerine `[` ve `]` kullanarak daha kısa bir sözdizimi elde edebilirsiniz. Örneğin, `if [ -f dosya.txt ]; then` şeklinde yazabilirsiniz.