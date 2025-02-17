# [Linux] Bash write penggunaan: Mengirim pesan ke pengguna lain

## Overview
Perintah `write` digunakan untuk mengirim pesan teks langsung ke terminal pengguna lain yang sedang aktif di sistem. Ini berguna untuk komunikasi cepat antar pengguna di lingkungan multi-user.

## Usage
Berikut adalah sintaks dasar dari perintah `write`:

```
write [nama_pengguna] [terminal]
```

## Common Options
- `-n`: Menonaktifkan pengiriman notifikasi ke pengguna yang menerima pesan.
- `-s`: Mengirim pesan dalam mode "silent", tanpa menampilkan informasi tentang pengirim.

## Common Examples

1. Mengirim pesan sederhana ke pengguna lain:
   ```bash
   write user1
   Halo, bagaimana kabarmu?
   ```

2. Mengirim pesan ke pengguna di terminal tertentu:
   ```bash
   write user2 pts/1
   Apakah kamu sudah selesai dengan tugasmu?
   ```

3. Menggunakan opsi `-n` untuk mengirim pesan tanpa notifikasi:
   ```bash
   write -n user3
   Ini adalah pesan tanpa notifikasi.
   ```

4. Mengirim pesan dalam mode "silent":
   ```bash
   write -s user4
   Pesan ini dikirim tanpa informasi pengirim.
   ```

## Tips
- Pastikan pengguna yang ingin Anda kirimi pesan sedang aktif dan tidak dalam mode "mesin mati" (logged out).
- Gunakan perintah `who` untuk melihat daftar pengguna yang sedang aktif dan terminal mereka sebelum mengirim pesan.
- Jika Anda tidak ingin mengganggu pengguna, pertimbangkan untuk mengirim pesan dengan cara lain, seperti email atau aplikasi pesan instan.