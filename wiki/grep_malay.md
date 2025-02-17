# [Linux] Bash grep Penggunaan: Mencari teks dalam fail

## Overview
Perintah `grep` digunakan untuk mencari dan memadankan teks dalam fail. Ia membolehkan pengguna untuk menapis baris yang mengandungi pola tertentu, menjadikannya alat yang sangat berguna untuk analisis data dan pengurusan sistem.

## Usage
Sintaks asas untuk menggunakan `grep` adalah seperti berikut:

```bash
grep [options] [arguments]
```

## Common Options
- `-i`: Mengabaikan kes (case insensitive).
- `-v`: Memaparkan baris yang tidak mengandungi pola yang dicari.
- `-r`: Mencari secara rekursif dalam direktori.
- `-n`: Memaparkan nombor baris bersama dengan hasil.
- `-l`: Memaparkan nama fail yang mengandungi pola yang dicari.

## Common Examples
Berikut adalah beberapa contoh penggunaan `grep`:

1. Mencari teks dalam fail:
   ```bash
   grep "teks" fail.txt
   ```

2. Mencari teks tanpa mengira kes:
   ```bash
   grep -i "teks" fail.txt
   ```

3. Mencari secara rekursif dalam direktori:
   ```bash
   grep -r "teks" /path/to/directory
   ```

4. Menunjukkan nombor baris bagi hasil:
   ```bash
   grep -n "teks" fail.txt
   ```

5. Menunjukkan nama fail yang mengandungi pola:
   ```bash
   grep -l "teks" *.txt
   ```

## Tips
- Gunakan `-i` untuk mencari tanpa mengira kes, terutamanya jika anda tidak pasti tentang huruf besar atau kecil.
- Untuk mencari lebih daripada satu pola, anda boleh menggunakan `-e` diikuti dengan pola yang berbeza.
- Jika anda ingin menyimpan hasil carian ke dalam fail, gunakan pengalihan output (`>`) untuk menyimpan hasilnya. Contoh:
  ```bash
  grep "teks" fail.txt > hasil.txt
  ```