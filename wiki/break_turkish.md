# [Linux] Bash break Kullanımı: Döngüden çıkmak için kullanılır

## Overview
`break` komutu, bir döngüden çıkmak için kullanılan bir Bash komutudur. Genellikle `for`, `while` veya `until` döngüleri içinde kullanılır ve döngünün çalışmasını sonlandırır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
break [n]
```

Burada `n`, döngü katmanını belirtir. Eğer `n` verilmezse, en içteki döngüden çıkılır.

## Common Options
- `n`: Çıkılacak döngü katmanını belirtir. Eğer birden fazla iç içe döngü varsa, hangi döngüden çıkılacağını kontrol etmek için kullanılır.

## Common Examples

### Örnek 1: Basit bir döngüden çıkma
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
Bu örnekte, `i` değişkeni 3 olduğunda döngüden çıkılır ve çıktıda sadece 1 ve 2 görünür.

### Örnek 2: İç içe döngülerde çıkma
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
Burada, `j` 2 olduğunda, her iki döngüden de çıkılır.

### Örnek 3: Kullanıcıdan giriş alarak döngüyü sonlandırma
```bash
while true; do
  read -p "Çıkmak için 'q' tuşuna basın: " input
  if [ "$input" = "q" ]; then
    break
  fi
  echo "Girdiğiniz: $input"
done
```
Bu örnekte, kullanıcı 'q' tuşuna bastığında döngü sonlanır.

## Tips
- `break` komutunu kullanırken, döngü katmanlarını dikkatlice planlayın, böylece hangi döngüden çıkmak istediğinizi net bir şekilde belirleyebilirsiniz.
- Karmaşık döngülerde `break` kullanırken, kodun okunabilirliğini artırmak için açıklayıcı yorumlar eklemeyi unutmayın.
- `break` komutunu, döngü içinde belirli bir koşul sağlandığında çıkmak için etkili bir şekilde kullanabilirsiniz.