# [Linux] Bash endif <Penggunaan setara>: Menyelesaikan blok kondisional

## Overview
Perintah `endif` dalam Bash digunakan untuk menandai akhir dari blok kondisional yang dimulai dengan perintah `if`. Ini membantu dalam mengorganisir dan mengelola alur logika dalam skrip Bash.

## Usage
Sintaks dasar dari perintah `endif` adalah sebagai berikut:

```bash
endif
```

## Common Options
Perintah `endif` tidak memiliki opsi tambahan. Ini hanya digunakan sebagai penutup untuk blok `if`.

## Common Examples

### Contoh 1: Menggunakan `if` dan `endif`
Berikut adalah contoh sederhana menggunakan `if` dan `endif` dalam skrip Bash:

```bash
#!/bin/bash

angka=10

if [ $angka -gt 5 ]; then
    echo "Angka lebih besar dari 5"
endif
```

### Contoh 2: Menggunakan `if` dengan `else` dan `endif`
Contoh berikut menunjukkan penggunaan `else` bersama dengan `endif`:

```bash
#!/bin/bash

angka=3

if [ $angka -gt 5 ]; then
    echo "Angka lebih besar dari 5"
else
    echo "Angka tidak lebih besar dari 5"
endif
```

## Tips
- Pastikan setiap blok `if` diakhiri dengan `endif` untuk menghindari kesalahan sintaks.
- Gunakan indentasi yang konsisten untuk meningkatkan keterbacaan skrip Anda.
- Selalu periksa kondisi logika Anda untuk memastikan bahwa skrip berjalan sesuai dengan yang diharapkan.