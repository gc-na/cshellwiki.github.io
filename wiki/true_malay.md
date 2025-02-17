# [Linux] Bash true penggunaan: Mengembalikan nilai benar

## Overview
Perintah `true` dalam Bash digunakan untuk mengembalikan nilai benar (exit status 0). Ia sering digunakan dalam skrip untuk menunjukkan bahawa sesuatu telah berjaya dilakukan tanpa sebarang ralat. Ini menjadikannya berguna dalam pelbagai situasi, seperti dalam pengendalian aliran logik dalam skrip.

## Usage
Berikut adalah sintaks asas untuk perintah `true`:

```bash
true [options] [arguments]
```

## Common Options
Perintah `true` tidak mempunyai pilihan khusus yang sering digunakan. Ia hanya berfungsi untuk mengembalikan nilai benar. Namun, anda boleh menggunakannya dalam konteks lain dengan pilihan yang mungkin bergantung kepada perintah lain yang digunakan bersamanya.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `true`:

1. **Menggunakan true dalam skrip:**
   ```bash
   if true; then
       echo "Ini akan selalu dicetak."
   fi
   ```

2. **Menggunakan true dalam loop:**
   ```bash
   while true; do
       echo "Ini akan terus dicetak sehingga dihentikan."
       sleep 1
   done
   ```

3. **Menggunakan true dengan perintah lain:**
   ```bash
   command || true
   ```

## Tips
- Gunakan `true` untuk memastikan bahawa skrip anda tidak terhenti apabila anda ingin teruskan walaupun terdapat ralat.
- Dalam konteks pengujian, `true` boleh digunakan untuk menguji aliran logik tanpa melibatkan sebarang operasi lain.
- Pastikan untuk menggunakan `true` dengan berhati-hati dalam loop, kerana ia akan menyebabkan loop berjalan tanpa henti jika tidak ada mekanisme untuk menghentikannya.