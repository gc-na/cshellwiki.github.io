# [Linux] Bash continue Kullanımı: Döngüdeki bir adımı atlama

## Overview
`continue` komutu, bir döngü içinde kullanıldığında, döngünün mevcut yinelemesini atlayarak bir sonraki yinelemeye geçilmesini sağlar. Bu, belirli bir koşulun sağlandığı durumlarda döngüdeki işlemleri atlamak için oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
continue [options]
```

## Common Options
`continue` komutunun kendisi için özel bir seçenek yoktur, ancak döngü yapısında kullanıldığında belirli koşullara bağlı olarak çalışır. Örneğin, `for`, `while` veya `until` döngüleri içinde kullanılabilir.

## Common Examples

### Örnek 1: Basit bir for döngüsü
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo "Sayı: $i"
done
```
Bu örnekte, `i` değişkeni 3 olduğunda `continue` komutu çalışır ve 3 sayısı atlanır. Çıktı:
```
Sayı: 1
Sayı: 2
Sayı: 4
Sayı: 5
```

### Örnek 2: While döngüsü ile kullanım
```bash
count=1
while [ $count -le 5 ]; do
    if [ $count -eq 2 ]; then
        count=$((count + 1))
        continue
    fi
    echo "Sayım: $count"
    count=$((count + 1))
done
```
Bu örnekte, 2 sayısı atlanır ve çıktı şu şekilde olur:
```
Sayım: 1
Sayım: 3
Sayım: 4
Sayım: 5
```

### Örnek 3: Kullanıcıdan girdi alma
```bash
for i in {1..5}; do
    read -p "Bir sayı girin: " num
    if [ $num -lt 0 ]; then
        echo "Negatif sayılar atlanıyor."
        continue
    fi
    echo "Girilen sayı: $num"
done
```
Bu örnekte, kullanıcı negatif bir sayı girdiğinde, `continue` komutu devreye girer ve döngü bir sonraki yinelemeye geçer.

## Tips
- `continue` komutunu kullanırken, döngüde hangi koşullarda atlama yapacağınızı iyi belirleyin.
- Kodun okunabilirliğini artırmak için `continue` komutunu kullanmadan önce koşulları net bir şekilde tanımlayın.
- Karmaşık döngülerde `continue` kullanımı, kodun akışını daha anlaşılır hale getirebilir.