# [Linux] Bash tput Penggunaan: Mengawal terminal dan output teks

## Overview
Perintah `tput` digunakan untuk mengawal terminal dan mengubah cara output teks dipaparkan. Ia membolehkan pengguna untuk mengubah warna teks, mengatur kedudukan kursor, dan melakukan pelbagai pengubahsuaian lain yang meningkatkan pengalaman pengguna di terminal.

## Usage
Berikut adalah sintaks asas untuk perintah `tput`:

```bash
tput [options] [arguments]
```

## Common Options
- `setaf`: Mengubah warna teks (foreground).
- `setab`: Mengubah warna latar belakang (background).
- `clear`: Membersihkan skrin terminal.
- `cup`: Menggerakkan kursor ke kedudukan tertentu.
- `bold`: Mengaktifkan teks tebal.

## Common Examples

1. **Mengubah warna teks menjadi merah:**
   ```bash
   tput setaf 1
   echo "Ini adalah teks merah"
   ```

2. **Mengubah warna latar belakang menjadi biru:**
   ```bash
   tput setab 4
   echo "Latar belakang ini biru"
   ```

3. **Membersihkan skrin terminal:**
   ```bash
   tput clear
   ```

4. **Menggerakkan kursor ke baris 5, kolum 10:**
   ```bash
   tput cup 5 10
   echo "Kursor berada di sini"
   ```

5. **Mengaktifkan teks tebal:**
   ```bash
   tput bold
   echo "Teks ini tebal"
   ```

## Tips
- Gunakan `tput reset` untuk mengembalikan semua pengubahsuaian terminal ke keadaan asal.
- Gabungkan beberapa perintah `tput` dalam skrip untuk mencipta pengalaman terminal yang lebih interaktif.
- Sentiasa periksa keserasian warna dan format pada terminal yang berbeza, kerana tidak semua terminal menyokong semua pilihan `tput`.