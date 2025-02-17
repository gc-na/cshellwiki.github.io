# [Linux] Bash chage Penggunaan: Mengelola Kebijakan Kedaluwarsa Kata Sandi

## Overview
Perintah `chage` digunakan untuk mengelola kebijakan kedaluwarsa kata sandi pada akun pengguna di sistem Linux. Dengan menggunakan perintah ini, administrator dapat mengatur berapa lama sebuah kata sandi dapat digunakan sebelum harus diubah oleh pengguna.

## Usage
Berikut adalah sintaks dasar dari perintah `chage`:

```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Menampilkan informasi tentang kebijakan kedaluwarsa kata sandi untuk pengguna tertentu.
- `-m, --mindays MIN_DAYS`: Mengatur jumlah hari minimum sebelum pengguna dapat mengubah kata sandi.
- `-M, --maxdays MAX_DAYS`: Mengatur jumlah hari maksimum sebelum kata sandi harus diubah.
- `-I, --inactive INACTIVE_DAYS`: Mengatur jumlah hari setelah kata sandi kedaluwarsa sebelum akun menjadi tidak aktif.
- `-E, --expiredate EXPIRE_DATE`: Mengatur tanggal kedaluwarsa akun pengguna.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `chage`:

1. **Menampilkan informasi kedaluwarsa kata sandi untuk pengguna:**
   ```bash
   chage -l username
   ```

2. **Mengatur maksimum hari penggunaan kata sandi menjadi 90 hari:**
   ```bash
   chage -M 90 username
   ```

3. **Mengatur minimum hari sebelum pengguna dapat mengubah kata sandi menjadi 7 hari:**
   ```bash
   chage -m 7 username
   ```

4. **Mengatur tanggal kedaluwarsa akun pengguna:**
   ```bash
   chage -E 2024-12-31 username
   ```

5. **Mengatur jumlah hari setelah kata sandi kedaluwarsa sebelum akun menjadi tidak aktif:**
   ```bash
   chage -I 30 username
   ```

## Tips
- Selalu periksa kebijakan keamanan organisasi Anda sebelum mengatur kebijakan kedaluwarsa kata sandi.
- Gunakan opsi `-l` untuk memverifikasi pengaturan setelah melakukan perubahan.
- Pertimbangkan untuk mengingatkan pengguna tentang perubahan kebijakan kedaluwarsa kata sandi agar mereka dapat mempersiapkan diri untuk mengubah kata sandi mereka tepat waktu.