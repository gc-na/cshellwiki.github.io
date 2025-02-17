# [Linux] Bash continue penggunaan: Melanjutkan pengulangan dalam skrip

## Overview
Perintah `continue` dalam Bash digunakan untuk melanjutkan iterasi seterusnya dalam pengulangan seperti `for`, `while`, atau `until`. Apabila `continue` dijalankan, pernyataan yang tersisa dalam blok pengulangan akan diabaikan, dan pengulangan akan berlanjut ke iterasi berikutnya.

## Usage
Berikut adalah sintaks asas untuk perintah `continue`:

```bash
continue [n]
```

Di mana `n` adalah nombor yang menunjukkan berapa banyak iterasi yang ingin dilanjutkan. Jika tidak ditentukan, `continue` akan melanjutkan ke iterasi seterusnya.

## Common Options
- `n`: Menentukan berapa banyak iterasi yang ingin dilewati. Contohnya, `continue 2` akan melanjutkan ke iterasi kedua seterusnya.

## Common Examples

### Contoh 1: Menggunakan continue dalam for loop
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo "Angka: $i"
done
```
Output:
```
Angka: 1
Angka: 2
Angka: 4
Angka: 5
```
Dalam contoh ini, apabila `i` sama dengan 3, perintah `continue` akan melanjutkan ke iterasi seterusnya, sehingga angka 3 tidak akan dicetak.

### Contoh 2: Menggunakan continue dalam while loop
```bash
count=0
while [ $count -lt 5 ]; do
    count=$((count + 1))
    if [ $count -eq 2 ]; then
        continue
    fi
    echo "Count: $count"
done
```
Output:
```
Count: 1
Count: 3
Count: 4
Count: 5
```
Di sini, apabila `count` adalah 2, perintah `continue` mengabaikan cetakan dan melanjutkan ke iterasi seterusnya.

### Contoh 3: Menggunakan continue dengan n
```bash
for i in {1..10}; do
    if [ $((i % 2)) -eq 0 ]; then
        continue 2
    fi
    echo "Odd number: $i"
done
```
Output:
```
Odd number: 1
Odd number: 3
Odd number: 5
Odd number: 7
Odd number: 9
```
Dalam contoh ini, apabila `i` adalah genap, perintah `continue 2` akan melanjutkan ke iterasi seterusnya dua kali, sehingga semua nombor genap diabaikan.

## Tips
- Gunakan `continue` untuk menghindari pelaksanaan kod tertentu dalam pengulangan tanpa perlu menggunakan banyak `if` bersarang.
- Pastikan untuk memahami konteks pengulangan anda agar `continue` tidak menyebabkan kekeliruan dalam aliran logik skrip.
- Sentiasa uji skrip anda dengan pelbagai senario untuk memastikan bahawa penggunaan `continue` berfungsi seperti yang diharapkan.