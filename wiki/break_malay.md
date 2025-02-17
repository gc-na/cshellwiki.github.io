# [Linux] Bash break penggunaan: Menghentikan pengulangan

## Overview
Perintah `break` dalam Bash digunakan untuk menghentikan pengulangan dalam struktur kawalan seperti `for`, `while`, atau `until`. Apabila `break` dijalankan, ia akan keluar dari blok pengulangan yang sedang aktif.

## Usage
Sintaks asas untuk menggunakan perintah `break` adalah seperti berikut:

```bash
break [n]
```

Di mana `n` adalah bilangan lapisan pengulangan yang ingin dihentikan. Jika `n` tidak ditentukan, `break` akan menghentikan pengulangan terdekat.

## Common Options
- `n`: Bilangan lapisan pengulangan yang ingin dihentikan. Jika tidak ditetapkan, hanya lapisan terdekat yang akan dihentikan.

## Common Examples

### Contoh 1: Menghentikan pengulangan `for`
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        break
    fi
    echo $i
done
```
*Output:*
```
1
2
```
Dalam contoh ini, pengulangan akan dihentikan apabila nilai `i` mencapai 3.

### Contoh 2: Menghentikan pengulangan `while`
```bash
count=1
while [ $count -le 5 ]; do
    if [ $count -eq 4 ]; then
        break
    fi
    echo $count
    ((count++))
done
```
*Output:*
```
1
2
3
```
Pengulangan `while` akan dihentikan apabila `count` mencapai 4.

### Contoh 3: Menggunakan `break` dengan `until`
```bash
num=1
until [ $num -gt 5 ]; do
    if [ $num -eq 3 ]; then
        break
    fi
    echo $num
    ((num++))
done
```
*Output:*
```
1
2
```
Dalam contoh ini, pengulangan `until` dihentikan apabila `num` mencapai 3.

## Tips
- Gunakan `break` untuk mengelakkan pengulangan yang tidak perlu dan menjadikan skrip lebih efisien.
- Sentiasa pastikan bahawa penggunaan `break` adalah dalam konteks yang sesuai untuk mengelakkan kekeliruan dalam aliran skrip.
- Jika anda ingin menghentikan lebih dari satu lapisan pengulangan, gunakan `break n` dengan nilai `n` yang sesuai.