# [Linux] Bash continue penggunaan: Melanjutkan eksekusi loop

## Overview
Perintah `continue` dalam Bash digunakan untuk melanjutkan eksekusi dari iterasi berikutnya dalam sebuah loop. Ketika `continue` dipanggil, perintah ini akan menghentikan eksekusi pernyataan yang tersisa dalam iterasi saat ini dan langsung melanjutkan ke iterasi berikutnya dari loop.

## Usage
Berikut adalah sintaks dasar dari perintah `continue`:

```
continue [n]
```

Di mana `n` adalah jumlah iterasi yang ingin dilewati. Jika `n` tidak ditentukan, maka `continue` akan melanjutkan ke iterasi berikutnya dari loop saat ini.

## Common Options
- `n`: Angka opsional yang menunjukkan berapa banyak iterasi yang ingin dilewati. Misalnya, `continue 2` akan melewatkan dua iterasi berikutnya.

## Common Examples

### Contoh 1: Menggunakan `continue` dalam loop for
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo "Nomor: $i"
done
```
Output:
```
Nomor: 1
Nomor: 2
Nomor: 4
Nomor: 5
```
Pada contoh ini, ketika nilai `i` sama dengan 3, perintah `continue` akan melewatkan eksekusi `echo` untuk iterasi tersebut.

### Contoh 2: Menggunakan `continue` dalam loop while
```bash
count=0
while [ $count -lt 5 ]; do
    count=$((count + 1))
    if [ $count -eq 2 ]; then
        continue
    fi
    echo "Hitungan: $count"
done
```
Output:
```
Hitungan: 1
Hitungan: 3
Hitungan: 4
Hitungan: 5
```
Di sini, ketika `count` mencapai 2, perintah `continue` akan melewatkan eksekusi `echo`.

### Contoh 3: Menggunakan `continue` dengan opsi
```bash
for i in {1..10}; do
    if [ $((i % 2)) -eq 0 ]; then
        continue 2
    fi
    echo "Bilangan ganjil: $i"
done
```
Output:
```
Bilangan ganjil: 1
Bilangan ganjil: 5
Bilangan ganjil: 9
```
Dalam contoh ini, jika `i` adalah bilangan genap, perintah `continue 2` akan melewatkan dua iterasi berikutnya.

## Tips
- Gunakan `continue` dengan bijak untuk meningkatkan keterbacaan kode Anda, terutama dalam loop yang kompleks.
- Pastikan untuk memahami bagaimana `continue` berinteraksi dengan kondisi dalam loop agar tidak melewatkan iterasi yang tidak diinginkan.
- Cobalah untuk menggunakan `continue` dalam kombinasi dengan pernyataan kondisi untuk mengontrol alur eksekusi dengan lebih baik.