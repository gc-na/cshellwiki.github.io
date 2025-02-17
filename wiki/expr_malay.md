# [Linux] Bash expr Penggunaan: Mengira nilai ekspresi

## Overview
Perintah `expr` dalam Bash digunakan untuk mengira nilai ekspresi aritmetik, membandingkan nilai, dan melakukan operasi string. Ia adalah alat yang berguna untuk pelbagai pengiraan dalam skrip shell.

## Usage
Berikut adalah sintaks asas untuk perintah `expr`:

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Menambah dua nombor.
- `-` : Mengurangkan nombor.
- `*` : Mengalikan nombor.
- `/` : Membahagikan nombor.
- `%` : Mengira baki pembahagian.
- `=` : Membandingkan dua nilai untuk kesamaan.
- `!=` : Membandingkan dua nilai untuk ketidak-samaan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `expr`:

1. **Menambah dua nombor:**
   ```bash
   expr 5 + 3
   ```
   Output: `8`

2. **Mengurangkan nombor:**
   ```bash
   expr 10 - 4
   ```
   Output: `6`

3. **Mengalikan nombor:**
   ```bash
   expr 7 \* 6
   ```
   Output: `42`

4. **Membahagikan nombor:**
   ```bash
   expr 20 / 4
   ```
   Output: `5`

5. **Mengira baki pembahagian:**
   ```bash
   expr 10 % 3
   ```
   Output: `1`

6. **Membandingkan dua nilai:**
   ```bash
   expr 5 = 5
   ```
   Output: `1` (benar)

7. **Membandingkan dua nilai untuk ketidak-samaan:**
   ```bash
   expr 5 != 3
   ```
   Output: `1` (benar)

## Tips
- Sentiasa gunakan `\` sebelum simbol `*` untuk mengelakkan konflik dengan pengembangan shell.
- Gunakan `$(...)` untuk menyimpan hasil `expr` dalam pembolehubah.
- Untuk operasi yang lebih kompleks, pertimbangkan untuk menggunakan `bc` atau `awk` yang menawarkan lebih banyak fungsi matematik.