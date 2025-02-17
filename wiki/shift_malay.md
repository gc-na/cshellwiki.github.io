# [Linux] Bash shift Penggunaan: Mengubah Posisi Parameter Posisi

## Overview
Perintah `shift` dalam Bash digunakan untuk menggeser parameter posisi ke kiri. Ini bermakna parameter pertama akan dihapus dan semua parameter yang lain akan bergerak satu posisi ke kiri. Ini berguna dalam skrip untuk mengakses argumen yang diberikan secara dinamik.

## Usage
Sintaks asas untuk perintah `shift` adalah seperti berikut:

```bash
shift [n]
```

Di mana `n` adalah bilangan yang menunjukkan berapa banyak posisi yang ingin diubah. Jika `n` tidak diberikan, `shift` akan menggeser satu posisi secara default.

## Common Options
- `n`: Bilangan yang menunjukkan berapa banyak posisi yang ingin diubah. Jika tidak ditentukan, ia akan menggeser satu posisi.

## Common Examples

### Contoh 1: Menggeser Satu Posisi
```bash
#!/bin/bash
echo "Sebelum shift: $1 $2 $3"
shift
echo "Selepas shift: $1 $2 $3"
```
Dalam contoh ini, jika skrip dijalankan dengan argumen `a b c`, outputnya akan menjadi:
```
Sebelum shift: a b c
Selepas shift: b c 
```

### Contoh 2: Menggeser Dua Posisi
```bash
#!/bin/bash
echo "Sebelum shift: $1 $2 $3"
shift 2
echo "Selepas shift: $1 $2 $3"
```
Jika dijalankan dengan argumen `x y z`, outputnya akan menjadi:
```
Sebelum shift: x y z
Selepas shift: z 
```

### Contoh 3: Menggunakan dalam Skrip
```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Parameter: $1"
    shift
done
```
Skrip ini akan mencetak semua parameter yang diberikan satu persatu.

## Tips
- Gunakan `shift` dalam skrip yang memerlukan pemprosesan argumen secara berulang.
- Pastikan untuk memeriksa bilangan parameter yang ada sebelum menggunakan `shift` untuk mengelakkan ralat.
- Kombinasikan `shift` dengan perintah lain seperti `while` untuk mengendalikan pengulangan dengan lebih baik.