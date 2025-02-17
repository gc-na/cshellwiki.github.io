# [Linux] Bash else Kullanımı: Koşullu ifadelerde alternatif yol

## Genel Bakış
`else` komutu, Bash betiklerinde koşullu ifadelerin bir parçası olarak kullanılır. `if` koşulu sağlanmadığında alternatif bir yol sunar. Bu, programın akışını kontrol etmek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
if [ koşul ]; then
    # koşul doğruysa çalışacak komutlar
else
    # koşul yanlışsa çalışacak komutlar
fi
```

## Yaygın Seçenekler
`else` komutunun kendine özgü seçenekleri yoktur, ancak `if` komutuyla birlikte kullanıldığında bazı koşul ifadeleri kullanılabilir:
- `-e`: Dosyanın var olup olmadığını kontrol eder.
- `-f`: Dosyanın bir dosya olup olmadığını kontrol eder.
- `-d`: Dosyanın bir dizin olup olmadığını kontrol eder.

## Yaygın Örnekler
1. **Basit bir koşul kontrolü:**
   ```bash
   if [ -e dosya.txt ]; then
       echo "dosya mevcut."
   else
       echo "dosya mevcut değil."
   fi
   ```

2. **Bir değişkenin kontrolü:**
   ```bash
   sayi=10
   if [ $sayi -gt 5 ]; then
       echo "Sayı 5'ten büyük."
   else
       echo "Sayı 5 veya daha küçük."
   fi
   ```

3. **Bir dizinin varlığını kontrol etme:**
   ```bash
   if [ -d /home/kullanici ]; then
       echo "Dizin mevcut."
   else
       echo "Dizin mevcut değil."
   fi
   ```

## İpuçları
- `else` ifadesini kullanırken, koşulun doğru veya yanlış olmasına göre hangi komutların çalışacağını dikkatlice planlayın.
- Koşul ifadelerini daha karmaşık hale getirmek için `elif` (else if) ifadesini kullanabilirsiniz.
- Betiklerinizi daha okunabilir hale getirmek için uygun girintileme ve yorum satırları eklemeyi unutmayın.