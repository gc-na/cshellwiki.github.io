# [Linux] Bash expr Penggunaan: Menghitung dan membandingkan ekspresi

## Overview
Perintah `expr` dalam Bash digunakan untuk mengevaluasi ekspresi aritmatika dan logika. Ini memungkinkan pengguna untuk melakukan operasi dasar seperti penjumlahan, pengurangan, perbandingan, dan manipulasi string.

## Usage
Berikut adalah sintaks dasar dari perintah `expr`:

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Menjumlahkan dua angka.
- `-` : Mengurangi angka kedua dari angka pertama.
- `*` : Mengalikan dua angka.
- `/` : Membagi angka pertama dengan angka kedua.
- `%` : Menghitung sisa dari pembagian dua angka.
- `=` : Membandingkan dua nilai untuk kesetaraan.
- `!=` : Membandingkan dua nilai untuk ketidaksetaraan.
- `<` : Memeriksa apakah nilai pertama kurang dari nilai kedua.
- `>` : Memeriksa apakah nilai pertama lebih besar dari nilai kedua.

## Common Examples
Berikut adalah beberapa contoh penggunaan `expr`:

### Contoh 1: Penjumlahan
Menjumlahkan dua angka:

```bash
expr 5 + 3
```

Output: `8`

### Contoh 2: Pengurangan
Mengurangi angka:

```bash
expr 10 - 4
```

Output: `6`

### Contoh 3: Perkalian
Mengalikan dua angka:

```bash
expr 7 \* 6
```

Output: `42`

### Contoh 4: Pembagian
Membagi angka:

```bash
expr 20 / 4
```

Output: `5`

### Contoh 5: Modulus
Menghitung sisa dari pembagian:

```bash
expr 10 % 3
```

Output: `1`

### Contoh 6: Perbandingan
Memeriksa kesetaraan:

```bash
expr 5 = 5
```

Output: `1` (true)

## Tips
- Selalu gunakan tanda backslash (`\`) sebelum operator `*` untuk menghindari kesalahan interpretasi oleh shell.
- Gunakan tanda kurung untuk mengelompokkan operasi jika melakukan lebih dari satu operasi dalam satu perintah.
- `expr` mengembalikan nilai 0 jika ekspresi benar dan 1 jika salah, yang dapat digunakan dalam skrip untuk pengkondisian.