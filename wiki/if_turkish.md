# [Linux] Bash if Kullanımı: Koşullu ifadeleri değerlendirme

## Genel Bakış
`if` komutu, Bash betiklerinde koşullu ifadeleri değerlendirmek için kullanılır. Belirli bir koşulun doğru olup olmadığını kontrol eder ve buna göre farklı komutlar çalıştırır. Bu, program akışını kontrol etmek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
if [ koşul ]; then
    # koşul doğruysa çalıştırılacak komutlar
else
    # koşul yanlışsa çalıştırılacak komutlar
fi
```

## Yaygın Seçenekler
- `-e`: Dosyanın var olup olmadığını kontrol eder.
- `-f`: Dosyanın bir dosya olup olmadığını kontrol eder.
- `-d`: Dosyanın bir dizin olup olmadığını kontrol eder.
- `-z`: Bir değişkenin boş olup olmadığını kontrol eder.
- `-gt`: Bir sayının diğerinden büyük olup olmadığını kontrol eder.
- `-lt`: Bir sayının diğerinden küçük olup olmadığını kontrol eder.

## Yaygın Örnekler

### Örnek 1: Dosyanın varlığını kontrol etme
```bash
if [ -e "dosya.txt" ]; then
    echo "Dosya mevcut."
else
    echo "Dosya mevcut değil."
fi
```

### Örnek 2: Bir değişkenin boş olup olmadığını kontrol etme
```bash
değişken=""
if [ -z "$değişken" ]; then
    echo "Değişken boştur."
else
    echo "Değişken doludur."
fi
```

### Örnek 3: Sayı karşılaştırması
```bash
sayı1=10
sayı2=20
if [ $sayı1 -lt $sayı2 ]; then
    echo "$sayı1, $sayı2'den küçüktür."
else
    echo "$sayı1, $sayı2'den büyük veya eşittir."
fi
```

## İpuçları
- Koşul ifadelerini yazarken boşluklara dikkat edin; `[` ve `]` arasında boşluk olmalıdır.
- Birden fazla koşul kontrolü yapmak için `elif` anahtar kelimesini kullanabilirsiniz.
- Daha karmaşık koşullar için `&&` (ve) ve `||` (veya) operatörlerini kullanarak birden fazla koşulu birleştirebilirsiniz.