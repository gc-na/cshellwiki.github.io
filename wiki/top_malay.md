# [Linux] Bash top Penggunaan: Memantau proses sistem

## Overview
Perintah `top` adalah alat yang digunakan untuk memantau proses yang sedang berjalan di sistem Linux. Ia memberikan gambaran masa nyata tentang penggunaan sumber daya sistem seperti CPU, memori, dan proses yang aktif. Dengan `top`, pengguna dapat melihat proses mana yang menggunakan sumber daya terbanyak dan melakukan pengurusan proses secara langsung.

## Usage
Sintaks asas untuk menggunakan perintah `top` adalah seperti berikut:

```bash
top [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `top`:

- `-d <delay>`: Menetapkan selang masa dalam saat antara kemas kini.
- `-n <number>`: Menentukan berapa kali `top` akan dikemas kini sebelum keluar.
- `-u <user>`: Menunjukkan hanya proses yang dimiliki oleh pengguna tertentu.
- `-p <pid>`: Memantau proses dengan ID proses tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `top`:

1. **Menjalankan `top` dengan kemas kini setiap 5 saat:**
   ```bash
   top -d 5
   ```

2. **Menjalankan `top` untuk memantau proses tertentu berdasarkan ID proses (PID):**
   ```bash
   top -p 1234
   ```

3. **Menjalankan `top` untuk melihat proses yang dimiliki oleh pengguna tertentu:**
   ```bash
   top -u username
   ```

4. **Menjalankan `top` dan menghentikannya selepas 10 kemas kini:**
   ```bash
   top -n 10
   ```

## Tips
- Gunakan `Shift + M` dalam antaramuka `top` untuk menyusun proses berdasarkan penggunaan memori.
- Tekan `q` untuk keluar dari antaramuka `top` dengan cepat.
- Perhatikan kolom `%CPU` dan `%MEM` untuk mengenal pasti proses yang memakan sumber daya tertinggi.
- Anda boleh menekan `h` dalam `top` untuk mendapatkan bantuan tentang pintasan dan fungsi lain yang tersedia.