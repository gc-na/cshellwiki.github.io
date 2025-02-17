# [Linux] Bash else penggunaan: Menangani kondisi alternatif dalam skrip

## Overview
Perintah `else` dalam Bash digunakan dalam struktur kontrol untuk menangani kondisi alternatif. Ini biasanya digunakan bersama dengan perintah `if` untuk menentukan apa yang harus dilakukan ketika kondisi yang diuji tidak terpenuhi.

## Usage
Sintaks dasar dari perintah `else` adalah sebagai berikut:

```bash
if [ kondisi ]; then
    # perintah jika kondisi benar
else
    # perintah jika kondisi salah
fi
```

## Common Options
Perintah `else` tidak memiliki opsi khusus, tetapi digunakan dalam konteks pernyataan `if`. Berikut adalah beberapa elemen yang sering digunakan bersamanya:

- `if`: Memulai pernyataan kondisi.
- `then`: Menunjukkan blok perintah yang akan dijalankan jika kondisi benar.
- `fi`: Menandai akhir dari pernyataan `if`.

## Common Examples

### Contoh 1: Menggunakan `else` untuk memeriksa file
```bash
if [ -f "file.txt" ]; then
    echo "File ada."
else
    echo "File tidak ada."
fi
```

### Contoh 2: Menggunakan `else` dengan variabel
```bash
read -p "Masukkan angka: " angka
if [ $angka -gt 10 ]; then
    echo "Angka lebih besar dari 10."
else
    echo "Angka 10 atau lebih kecil."
fi
```

### Contoh 3: Menggunakan `else` dalam skrip
```bash
#!/bin/bash
read -p "Apakah Anda ingin melanjutkan? (ya/tidak): " jawaban
if [ "$jawaban" == "ya" ]; then
    echo "Melanjutkan..."
else
    echo "Berhenti."
fi
```

## Tips
- Selalu gunakan tanda kurung untuk membungkus kondisi dalam pernyataan `if`.
- Pastikan untuk menutup pernyataan `if` dengan `fi` untuk menghindari kesalahan sintaks.
- Gunakan indentasi yang konsisten untuk meningkatkan keterbacaan skrip Anda.