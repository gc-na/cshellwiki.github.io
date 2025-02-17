# [Linux] Bash pr: [format dan cetak fail teks]

## Overview
Perintah `pr` dalam Bash digunakan untuk memformat dan mencetak fail teks. Ia membolehkan pengguna untuk menyusun teks dalam bentuk yang lebih teratur, menjadikannya lebih mudah dibaca dan dicetak.

## Usage
Berikut adalah sintaks asas untuk perintah `pr`:

```bash
pr [options] [arguments]
```

## Common Options
- `-h`: Menetapkan tajuk untuk halaman.
- `-l`: Menentukan bilangan baris setiap halaman.
- `-w`: Menentukan lebar halaman.
- `-t`: Mengabaikan cetakan tajuk dan nombor halaman.
- `-s`: Menentukan pemisah antara lajur.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `pr`:

1. **Mencetak fail teks dengan tajuk:**
   ```bash
   pr -h "Tajuk Fail" fail.txt
   ```

2. **Mencetak fail dengan 50 baris setiap halaman:**
   ```bash
   pr -l 50 fail.txt
   ```

3. **Mengabaikan tajuk dan nombor halaman:**
   ```bash
   pr -t fail.txt
   ```

4. **Mencetak dua fail dalam lajur:**
   ```bash
   pr file1.txt file2.txt
   ```

5. **Menetapkan lebar halaman kepada 100:**
   ```bash
   pr -w 100 fail.txt
   ```

## Tips
- Gunakan pilihan `-h` untuk menambah tajuk yang relevan pada cetakan anda.
- Pastikan untuk menguji pilihan `-l` untuk menyesuaikan bilangan baris yang sesuai dengan keperluan cetakan anda.
- Jika anda ingin mencetak lebih dari satu fail dalam lajur, pastikan fail tersebut mempunyai format yang serupa untuk hasil yang lebih baik.