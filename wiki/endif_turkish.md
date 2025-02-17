# [Linux] Bash endif kullanımı: Koşullu ifadeleri sonlandırma

## Genel Bakış
`endif` komutu, bir koşullu ifadenin sonunu belirtmek için kullanılır. Genellikle `if` yapıları içinde kullanılır ve bir koşulun değerlendirilmesinin ardından hangi kod bloğunun çalıştırılacağını belirlemek için önemlidir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
endif
```

## Yaygın Seçenekler
`endif` komutunun kendisi için özel bir seçenek yoktur, çünkü bu komut yalnızca bir koşulun sonunu belirtir. Ancak, `if` komutuyla birlikte kullanıldığında, `if` komutunun seçenekleri geçerli olur.

## Yaygın Örnekler
Aşağıda `endif` komutunun nasıl kullanılacağına dair bazı örnekler bulunmaktadır:

### Örnek 1: Basit bir koşul
```bash
if [ "$a" -lt 10 ]; then
    echo "a 10'dan küçüktür."
endif
```

### Örnek 2: Birden fazla koşul
```bash
if [ "$a" -lt 10 ]; then
    echo "a 10'dan küçüktür."
elif [ "$a" -eq 10 ]; then
    echo "a 10'a eşittir."
else
    echo "a 10'dan büyüktür."
endif
```

### Örnek 3: Koşul içinde bir komut çalıştırma
```bash
if [ -f "dosya.txt" ]; then
    echo "Dosya mevcut."
endif
```

## İpuçları
- `endif` komutunu kullanırken, her `if` ifadesinin bir `endif` ile kapatıldığından emin olun.
- Koşul ifadelerinizi daha okunabilir hale getirmek için uygun boşluk ve girintileri kullanın.
- Karmaşık koşul yapılarında, kodunuzu daha iyi organize etmek için `then` ve `endif` arasına açıklayıcı yorumlar ekleyin.